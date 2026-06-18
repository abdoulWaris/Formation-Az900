# 02 - Azure Architecture

## Introduction

L'architecture Azure repose sur une infrastructure mondiale composée de centres de données répartis dans plusieurs régions. Cette architecture permet d'offrir des services hautement disponibles, sécurisés et évolutifs.

---

## 1. Les Régions Azure

Une région Azure est un ensemble de centres de données situés dans une même zone géographique.

Exemples :

* France Central
* West Europe
* North Europe
* East US

### Pourquoi les régions sont importantes ?

* Réduction de la latence
* Respect des exigences de conformité
* Amélioration de la disponibilité

---

## 2. Les Zones de Disponibilité

Les Zones de Disponibilité (Availability Zones) sont des centres de données physiquement séparés au sein d'une même région.

Chaque zone dispose :

* D'une alimentation électrique indépendante
* D'un système de refroidissement indépendant
* D'un réseau indépendant

### Avantages

* Tolérance aux pannes
* Haute disponibilité
* Réduction des interruptions de service

---

## 3. Les Paires de Régions

Microsoft associe certaines régions par paires afin d'assurer la continuité des services en cas de catastrophe majeure.

Exemple :

* France Central ↔ France South
* North Europe ↔ West Europe

### Avantages

* Réplication des données
* Reprise après sinistre (Disaster Recovery)
* Maintenance coordonnée

---

## 4. Les Ressources Azure

Une ressource Azure est un élément que vous créez dans Azure.

Exemples :

* Machine virtuelle (VM)
* Compte de stockage
* Base de données
* Réseau virtuel

---

## 5. Les Groupes de Ressources (Resource Groups)

Un Resource Group est un conteneur logique permettant de regrouper des ressources Azure.

Exemple :

Resource Group :

* VM-Web
* StorageAccount
* Virtual Network

### Avantages

* Gestion simplifiée
* Contrôle des accès
* Suppression groupée des ressources

---

## 6. Les Abonnements (Subscriptions)

Un abonnement Azure est une unité de facturation et de gestion.

Il permet :

* De suivre les coûts
* D'appliquer des limites
* D'organiser les ressources

Une organisation peut posséder plusieurs abonnements.

---

## 7. Les Groupes d’Administration (Management Groups)

Les Management Groups permettent d'organiser plusieurs abonnements.

Structure :

Tenant
└── Management Group
├── Subscription A
└── Subscription B

### Avantages

* Gouvernance centralisée
* Application des politiques à grande échelle

---

## 8. Azure Resource Manager (ARM)

Azure Resource Manager est le service de gestion des ressources Azure.

Fonctions principales :

* Déploiement des ressources
* Gestion des permissions
* Organisation des ressources

ARM utilise des modèles appelés ARM Templates pour automatiser les déploiements.

---

## Hiérarchie Azure

Tenant
└── Management Group
└── Subscription
└── Resource Group
└── Resources

---

## Résumé

L'architecture Azure repose sur plusieurs composants clés :

* Régions
* Zones de disponibilité
* Resource Groups
* Subscriptions
* Management Groups
* Azure Resource Manager

Ces éléments permettent d'organiser, sécuriser et administrer efficacement les ressources dans Azure.

---

## À retenir pour l'examen AZ-900

* Différence entre Région et Zone de Disponibilité
* Rôle d'un Resource Group
* Fonction d'une Subscription
* Hiérarchie Azure
* Azure Resource Manager (ARM)
