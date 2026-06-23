# 07 - Azure Security

## Introduction

La sécurité est une responsabilité partagée entre Microsoft et le client.

Microsoft protège l'infrastructure physique Azure, tandis que le client reste responsable de la sécurité de ses données, identités, applications et configurations.

Comprendre les services de sécurité Azure est essentiel pour réussir l'examen AZ-900.

---

## 1. Le Modèle de Responsabilité Partagée

Selon le modèle utilisé (IaaS, PaaS ou SaaS), les responsabilités sont réparties différemment.

### IaaS

Le client gère :

* Système d'exploitation
* Applications
* Données
* Comptes utilisateurs

Microsoft gère :

* Datacenters
* Réseau physique
* Serveurs physiques

---

### PaaS

Le client gère :

* Applications
* Données

Microsoft gère :

* Infrastructure
* Système d'exploitation
* Runtime

---

### SaaS

Microsoft gère presque tout.

Le client gère principalement :

* Les utilisateurs
* Les données
* Les paramètres métier

---

## 2. Microsoft Entra ID (anciennement Azure Active Directory)

Microsoft Entra ID est le service de gestion des identités et des accès d'Azure.

---

### Fonctionnalités

* Authentification
* Autorisation
* Gestion des utilisateurs
* Gestion des groupes

---

### Cas d'utilisation

* Connexion aux applications Azure
* Single Sign-On (SSO)
* Gestion centralisée des identités

---

## 3. Multi-Factor Authentication (MFA)

Le MFA ajoute une couche de sécurité supplémentaire.

L'utilisateur doit fournir plusieurs preuves d'identité.

---

### Exemple

* Mot de passe
* Code SMS ou application mobile

---

### Avantages

* Réduction des risques de compromission
* Protection contre le vol de mots de passe

---

## 4. Single Sign-On (SSO)

Le SSO permet d'accéder à plusieurs applications avec une seule authentification.

---

### Avantages

* Meilleure expérience utilisateur
* Réduction du nombre de mots de passe
* Sécurité améliorée

---

## 5. Role-Based Access Control (RBAC)

RBAC permet d'attribuer des permissions selon un rôle.

---

### Exemples de rôles

#### Owner

* Contrôle total

#### Contributor

* Gestion des ressources
* Pas de gestion des accès

#### Reader

* Lecture uniquement

---

### Avantages

* Principe du moindre privilège
* Contrôle précis des accès

---

## 6. Azure Key Vault

Azure Key Vault permet de stocker de manière sécurisée :

* Secrets
* Mots de passe
* Certificats
* Clés de chiffrement

---

### Cas d'utilisation

* Stockage des chaînes de connexion
* Gestion des certificats SSL
* Protection des secrets applicatifs

---

## 7. Microsoft Defender for Cloud

Microsoft Defender for Cloud est un service de gestion de la posture de sécurité.

---

### Fonctionnalités

* Recommandations de sécurité
* Détection des menaces
* Évaluation des vulnérabilités
* Protection des ressources Azure

---

### Exemple

Le service peut détecter :

* Port ouvert inutilement
* Configuration non sécurisée
* VM vulnérable

---

## 8. Microsoft Sentinel

Microsoft Sentinel est une solution SIEM et SOAR basée sur le cloud.

---

### SIEM

Security Information and Event Management

Collecte et analyse les journaux de sécurité.

---

### SOAR

Security Orchestration, Automation and Response

Automatise les réponses aux incidents.

---

### Avantages

* Détection centralisée
* Analyse des menaces
* Réponse automatisée

---

## 9. Azure Firewall

Azure Firewall est un service de pare-feu managé.

---

### Fonctionnalités

* Filtrage du trafic réseau
* Contrôle des accès
* Journalisation

---

### Avantages

* Haute disponibilité
* Administration centralisée

---

## 10. Network Security Groups (NSG)

Les NSG permettent de contrôler le trafic entrant et sortant.

---

### Exemple

Autoriser :

* HTTPS (443)

Bloquer :

* SSH depuis Internet

---

## 11. Chiffrement des données

Azure protège les données grâce au chiffrement.

---

### Chiffrement au repos

Les données stockées sont chiffrées automatiquement.

Exemples :

* Blob Storage
* Disques VM
* Bases de données

---

### Chiffrement en transit

Les communications utilisent :

* HTTPS
* TLS

---

## 12. Azure DDoS Protection

Azure DDoS Protection protège les applications contre les attaques par déni de service distribué.

---

### Objectif

Maintenir la disponibilité des applications même en cas d'attaque.

---

### Avantages

* Protection automatique
* Surveillance continue
* Réduction des interruptions

---

## 13. Zero Trust

Zero Trust est un modèle de sécurité moderne.

Principe :

> Ne jamais faire confiance, toujours vérifier.

---

### Les piliers

* Vérification explicite
* Moindre privilège
* Supposition de compromission

---

## Architecture Sécurité Azure

Utilisateur
↓
Microsoft Entra ID
↓
MFA
↓
RBAC
↓
Application Azure
↓
Key Vault
↓
Données chiffrées

---

## Résumé

Les principaux services de sécurité Azure sont :

* Microsoft Entra ID
* MFA
* SSO
* RBAC
* Azure Key Vault
* Microsoft Defender for Cloud
* Microsoft Sentinel
* Azure Firewall
* Azure DDoS Protection

Ces services permettent de sécuriser les identités, les applications et les données dans Azure.

---

## À retenir pour l'examen AZ-900

### Gestion des identités

* Microsoft Entra ID
* SSO
* MFA

### Gestion des accès

* RBAC
* Principe du moindre privilège

### Protection des données

* Chiffrement au repos
* Chiffrement en transit
* Azure Key Vault

### Protection des ressources

* Microsoft Defender for Cloud
* Azure Firewall
* Azure DDoS Protection

### Supervision sécurité

* Microsoft Sentinel

---

## Questions fréquentes AZ-900

**Je veux gérer les utilisateurs et les groupes dans Azure**

→ Microsoft Entra ID

**Je veux sécuriser les mots de passe et certificats**

→ Azure Key Vault

**Je veux donner uniquement des droits de lecture**

→ Rôle Reader (RBAC)

**Je veux ajouter une vérification supplémentaire à la connexion**

→ MFA

**Je veux recevoir des recommandations de sécurité pour mes ressources**

→ Microsoft Defender for Cloud

**Je veux centraliser et analyser les journaux de sécurité**

→ Microsoft Sentinel

**Je veux protéger une application contre les attaques DDoS**

→ Azure DDoS Protection
