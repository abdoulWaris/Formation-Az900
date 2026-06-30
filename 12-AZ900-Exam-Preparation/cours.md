# 12 - AZ-900 Exam Preparation

## Introduction

Félicitations ! 🎉

Vous avez terminé les principaux chapitres de cette formation AZ-900.

Ce dernier chapitre est consacré à la préparation de l'examen. Il récapitule les concepts essentiels, les pièges fréquents et propose des questions similaires à celles rencontrées lors de la certification.

---

# 1. Les notions indispensables

## Cloud Concepts

Vous devez connaître :

* Les avantages du Cloud
* Les modèles de déploiement

  * Public Cloud
  * Private Cloud
  * Hybrid Cloud
* Les modèles de services

  * IaaS
  * PaaS
  * SaaS
* Scalabilité
* Élasticité
* Haute disponibilité

---

## Azure Architecture

À retenir :

* Région Azure
* Availability Zone
* Region Pair
* Resource Group
* Subscription
* Management Group
* Azure Resource Manager (ARM)

---

## Compute

Connaître la différence entre :

| Service                    | Utilisation                    |
| -------------------------- | ------------------------------ |
| Virtual Machines           | Contrôle total du serveur      |
| App Service                | Hébergement d'applications web |
| Azure Functions            | Exécution de code à la demande |
| Azure Container Instances  | Conteneur unique               |
| Azure Kubernetes Service   | Orchestration de conteneurs    |
| Virtual Machine Scale Sets | Auto-scaling des VM            |

---

## Networking

À connaître :

* Virtual Network
* Subnet
* NSG
* VPN Gateway
* ExpressRoute
* Load Balancer
* Application Gateway
* Traffic Manager
* CDN

---

## Storage

Connaître les différences entre :

| Service       | Utilisation               |
| ------------- | ------------------------- |
| Blob Storage  | Images, vidéos, documents |
| Azure Files   | Partage de fichiers       |
| Queue Storage | Messagerie                |
| Table Storage | Base NoSQL simple         |
| Disk Storage  | Disques des VM            |

---

## Security

Les services incontournables :

* Microsoft Entra ID
* MFA
* SSO
* RBAC
* Azure Key Vault
* Microsoft Defender for Cloud
* Microsoft Sentinel

---

## Governance

À connaître :

* Azure Policy
* Initiative
* Resource Locks
* Tags
* ARM Templates
* Microsoft Purview
* Compliance Manager

---

## Cost Management

Connaître :

* Pricing Calculator
* TCO Calculator
* Cost Management
* Budgets
* Alerts
* Reserved Instances
* Spot Virtual Machines

---

## Monitoring

À retenir :

* Azure Monitor
* Metrics
* Logs
* Log Analytics
* Application Insights
* Azure Advisor
* Service Health
* Resource Health

---

# 2. Les différences à connaître

## VM vs App Service

| Virtual Machines   | App Service           |
| ------------------ | --------------------- |
| IaaS               | PaaS                  |
| Gestion du système | Azure gère le système |
| Contrôle total     | Déploiement simplifié |

---

## App Service vs Azure Functions

| App Service          | Functions                   |
| -------------------- | --------------------------- |
| Application complète | Fonction unique             |
| Toujours disponible  | Déclenchée par un événement |

---

## Blob Storage vs Azure Files

| Blob              | Files                   |
| ----------------- | ----------------------- |
| Stockage d'objets | Partage de fichiers SMB |

---

## VPN Gateway vs ExpressRoute

| VPN                | ExpressRoute     |
| ------------------ | ---------------- |
| Passe par Internet | Connexion privée |
| Moins coûteux      | Plus performant  |

---

## Load Balancer vs Application Gateway

| Load Balancer      | Application Gateway   |
| ------------------ | --------------------- |
| Niveau 4 (TCP/UDP) | Niveau 7 (HTTP/HTTPS) |
| Répartition réseau | Routage web + WAF     |

---

## Azure Monitor vs Azure Advisor

| Monitor     | Advisor         |
| ----------- | --------------- |
| Supervision | Recommandations |

---

## Azure Backup vs Azure Site Recovery

| Backup     | Site Recovery          |
| ---------- | ---------------------- |
| Sauvegarde | Reprise après sinistre |

---

## Vertical vs Horizontal Scaling

| Vertical        | Horizontal       |
| --------------- | ---------------- |
| Plus de CPU/RAM | Plus de machines |

---

# 3. Questions type AZ-900

## Question 1

Vous souhaitez héberger un site web sans gérer de serveur.

**Réponse :**

Azure App Service

---

## Question 2

Vous souhaitez stocker des images et des vidéos.

**Réponse :**

Azure Blob Storage

---

## Question 3

Vous souhaitez exécuter du code uniquement lorsqu'un événement se produit.

**Réponse :**

Azure Functions

---

## Question 4

Vous souhaitez connecter votre entreprise à Azure via une connexion privée.

**Réponse :**

ExpressRoute

---

## Question 5

Vous souhaitez attribuer des permissions selon les rôles des utilisateurs.

**Réponse :**

RBAC

---

## Question 6

Vous souhaitez empêcher la suppression accidentelle d'une ressource.

**Réponse :**

Resource Lock

---

## Question 7

Vous souhaitez surveiller les performances de vos ressources Azure.

**Réponse :**

Azure Monitor

---

## Question 8

Vous souhaitez estimer le coût d'un projet Azure avant son déploiement.

**Réponse :**

Azure Pricing Calculator

---

## Question 9

Vous souhaitez gérer des conteneurs Kubernetes.

**Réponse :**

Azure Kubernetes Service (AKS)

---

## Question 10

Vous souhaitez protéger les secrets et certificats de votre application.

**Réponse :**

Azure Key Vault

---

# 4. Les pièges de l'examen

### Azure Functions ≠ App Service

Functions exécute du code à la demande.

App Service héberge une application complète.

---

### VPN Gateway ≠ ExpressRoute

VPN utilise Internet.

ExpressRoute utilise une connexion privée.

---

### Azure Monitor ≠ Azure Advisor

Monitor collecte des données.

Advisor fournit des recommandations.

---

### Azure Backup ≠ Site Recovery

Backup sauvegarde les données.

Site Recovery redémarre les applications dans une autre région.

---

### Blob Storage ≠ Azure Files

Blob = objets.

Files = partage de fichiers.

---

### Azure Policy ≠ RBAC

Policy définit ce qui peut être créé.

RBAC définit qui peut agir sur les ressources.

---

# 5. Conseils pour réussir l'examen

* Lire attentivement chaque question.
* Identifier les mots-clés (sécurité, stockage, réseau, coût, supervision…).
* Éliminer les réponses manifestement incorrectes.
* Se concentrer sur le besoin métier avant de choisir un service.
* Bien connaître les différences entre les services Azure.

---

# 6. Cheat Sheet AZ-900

## Compute

* VM → IaaS
* App Service → PaaS
* Functions → Serverless
* AKS → Kubernetes
* ACI → Conteneur

---

## Storage

* Blob → Objets
* Files → Partage SMB
* Queue → Messages
* Table → NoSQL
* Disk → Disques VM

---

## Networking

* VNet → Réseau privé
* NSG → Pare-feu
* VPN → Internet
* ExpressRoute → Connexion privée
* Load Balancer → Répartition réseau
* Application Gateway → HTTP/HTTPS
* Traffic Manager → Routage DNS
* CDN → Distribution de contenu

---

## Security

* Entra ID → Identités
* MFA → Double authentification
* RBAC → Permissions
* Key Vault → Secrets
* Defender for Cloud → Sécurité
* Sentinel → SIEM / SOAR

---

## Governance

* Policy → Règles
* Initiative → Groupe de Policies
* Tags → Organisation
* Resource Locks → Protection
* ARM → Déploiement

---

## Monitoring

* Azure Monitor → Supervision
* Metrics → Données temps réel
* Logs → Journaux
* Log Analytics → Analyse
* Advisor → Recommandations

---

## Cost Management

* Pricing Calculator → Estimation
* TCO Calculator → Comparaison
* Budgets → Limites
* Cost Management → Analyse
* Reserved Instances → Réduction des coûts

---

# Félicitations 🎉

Vous disposez maintenant d'une vue d'ensemble des concepts fondamentaux d'Azure couverts par la certification **Microsoft Azure Fundamentals (AZ-900)**.

Cette formation vous a permis de découvrir :

* Les concepts du Cloud Computing
* L'architecture Azure
* Les principaux services Azure
* Les bonnes pratiques de sécurité
* La gouvernance
* La gestion des coûts
* La supervision
* Les notions de disponibilité et de résilience

Vous êtes désormais prêt à passer la certification **AZ-900** ou à approfondir vos connaissances avec des certifications plus avancées comme **AZ-104 (Azure Administrator)** ou **AZ-204 (Azure Developer)**.

Bonne chance pour votre examen ! 🚀
