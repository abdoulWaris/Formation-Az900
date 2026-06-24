# 08 - Azure Governance & Compliance

## Introduction

La gouvernance (Governance) permet d'assurer que les ressources Azure sont utilisées conformément aux règles de l'entreprise.

Elle aide à :

* Contrôler les coûts
* Renforcer la sécurité
* Garantir la conformité
* Standardiser les déploiements

Pour l'examen AZ-900, il est important de comprendre les principaux outils de gouvernance proposés par Azure.

---

## 1. Hiérarchie Azure

Les ressources Azure sont organisées selon une hiérarchie.

```
Tenant
└── Management Group
    └── Subscription
        └── Resource Group
            └── Resources
```

---

### Tenant

Représente l'organisation dans Microsoft Entra ID.

---

### Management Group

Permet de regrouper plusieurs abonnements afin d'appliquer des règles communes.

---

### Subscription

Unité de facturation et de gestion.

---

### Resource Group

Conteneur logique regroupant plusieurs ressources Azure.

---

### Resource

Exemples :

* Machine Virtuelle
* Base de données
* Compte de stockage

---

## 2. Azure Policy

Azure Policy permet d'imposer des règles sur les ressources Azure.

---

### Exemples

Autoriser uniquement :

* Les régions européennes
* Les VM approuvées
* Les ressources taguées

---

### Cas d'utilisation

Empêcher :

* Les ressources non conformes
* Les configurations interdites

---

### Avantages

* Gouvernance automatisée
* Conformité renforcée
* Réduction des erreurs

---

## 3. Azure Initiative

Une Initiative est un regroupement de plusieurs Azure Policies.

---

### Exemple

Initiative "Sécurité"

Contient :

* Chiffrement obligatoire
* MFA obligatoire
* Sauvegarde activée

---

### Avantages

* Gestion simplifiée
* Application cohérente des règles

---

## 4. Resource Locks

Les Resource Locks empêchent certaines actions sur les ressources.

---

### Types de verrouillage

#### CanNotDelete

Empêche la suppression.

---

#### ReadOnly

Empêche toute modification.

---

### Cas d'utilisation

* Bases de données critiques
* Réseaux de production
* Applications sensibles

---

## 5. Tags

Les Tags sont des paires clé/valeur ajoutées aux ressources.

---

### Exemple

```
Environment = Production
Project = E-Commerce
Owner = IT Team
```

---

### Avantages

* Organisation des ressources
* Reporting
* Suivi des coûts

---

## 6. Azure Blueprints

Azure Blueprints permet de déployer rapidement des environnements conformes aux standards de l'entreprise.

---

### Peut inclure

* Policies
* RBAC
* Templates ARM
* Resource Groups

---

### Avantages

* Standardisation
* Déploiement rapide
* Réduction des erreurs

---

## 7. Microsoft Purview

Microsoft Purview est une solution de gouvernance et de gestion des données.

---

### Fonctionnalités

* Classification des données
* Découverte des données
* Catalogage
* Conformité

---

### Cas d'utilisation

* Gouvernance des données
* Protection des informations sensibles

---

## 8. Compliance Manager

Compliance Manager aide à évaluer le niveau de conformité d'une organisation.

---

### Domaines couverts

* RGPD (GDPR)
* ISO 27001
* NIST
* HIPAA

---

### Fonctionnalités

* Évaluation des risques
* Recommandations
* Score de conformité

---

## 9. Service Trust Portal

Le Service Trust Portal fournit des informations sur :

* La sécurité Azure
* Les certifications
* Les audits
* Les rapports de conformité

---

### Exemples de certifications

* ISO 27001
* SOC
* GDPR
* PCI DSS

---

## 10. Azure Resource Manager (ARM)

Azure Resource Manager est le moteur de gestion des ressources Azure.

---

### Fonctionnalités

* Déploiement
* Organisation
* Contrôle des accès

---

### ARM Templates

Permettent de déployer une infrastructure sous forme de code (IaC).

---

### Exemple

Déploiement automatique :

* Réseau
* VM
* Base de données

En une seule opération.

---

## Gouvernance dans Azure

Les outils principaux sont :

| Outil              | Rôle                       |
| ------------------ | -------------------------- |
| Azure Policy       | Contrôle des règles        |
| Initiative         | Groupe de Policies         |
| Resource Locks     | Protection des ressources  |
| Tags               | Organisation               |
| Blueprints         | Standardisation            |
| Purview            | Gouvernance des données    |
| Compliance Manager | Conformité                 |
| ARM                | Déploiement des ressources |

---

## Exemple d'entreprise

Une entreprise souhaite :

* Autoriser uniquement les régions européennes
* Empêcher la suppression des bases de données
* Identifier les ressources de production

Solution :

* Azure Policy
* Resource Locks
* Tags

---

## Résumé

Azure Governance permet de :

* Contrôler les ressources
* Standardiser les déploiements
* Réduire les risques
* Garantir la conformité

Les principaux outils sont :

* Azure Policy
* Initiatives
* Resource Locks
* Tags
* Blueprints
* Purview
* Compliance Manager

---

## À retenir pour l'examen AZ-900

### Gouvernance

* Azure Policy = appliquer des règles
* Initiative = groupe de Policies
* Tags = organiser les ressources
* Resource Locks = protéger les ressources

### Conformité

* Compliance Manager
* Service Trust Portal
* Microsoft Purview

### Déploiement

* Azure Resource Manager (ARM)
* ARM Templates

---

## Questions fréquentes AZ-900

**Je veux empêcher la création de VM dans certaines régions**

→ Azure Policy

**Je veux appliquer plusieurs règles de sécurité en une seule fois**

→ Azure Initiative

**Je veux empêcher la suppression accidentelle d'une base de données**

→ Resource Lock (CanNotDelete)

**Je veux organiser les ressources par projet ou environnement**

→ Tags

**Je veux vérifier la conformité RGPD de mon environnement**

→ Compliance Manager

**Je veux consulter les certifications de sécurité Azure**

→ Service Trust Portal

**Je veux déployer mon infrastructure automatiquement**

→ ARM Templates
