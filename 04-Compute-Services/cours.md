# 04 - Compute Services

## Introduction

Les services de calcul (Compute) permettent d'exécuter des applications, des conteneurs et des machines virtuelles dans Azure.

Azure propose plusieurs solutions adaptées à différents besoins :

* Contrôle total de l'infrastructure
* Hébergement d'applications web
* Exécution de conteneurs
* Services serverless

Le choix dépend du niveau de gestion souhaité et des exigences de l'application.

---

## 1. Azure Virtual Machines (VM)

Azure Virtual Machines permet de créer des serveurs Windows ou Linux dans le cloud.

Il s'agit d'un service **IaaS (Infrastructure as a Service)**.

### Ce que Microsoft gère

* Infrastructure physique
* Réseau physique
* Centres de données

### Ce que vous gérez

* Système d'exploitation
* Applications
* Configuration serveur
* Correctifs logiciels

---

### Cas d'utilisation

* Migration d'applications existantes
* Hébergement de serveurs web
* Serveurs de bases de données
* Environnements de test

---

### Avantages

* Contrôle total
* Flexibilité maximale
* Compatible avec presque tous les logiciels

---

## 2. Virtual Machine Scale Sets (VMSS)

Les Virtual Machine Scale Sets permettent de déployer plusieurs VM identiques.

Azure peut automatiquement :

* Ajouter des VM
* Supprimer des VM
* Répartir la charge

---

### Exemple

Une application reçoit beaucoup de trafic :

* 2 VM en période normale
* 10 VM pendant les pics d'utilisation

---

### Avantages

* Haute disponibilité
* Auto-scaling
* Réduction des coûts

---

## 3. Azure App Service

Azure App Service permet d'héberger des applications web sans gérer les serveurs.

Il s'agit d'un service **PaaS (Platform as a Service)**.

---

### Langages supportés

* Java
* .NET
* Node.js
* Python
* PHP

---

### Fonctionnalités

* Déploiement simplifié
* Certificats SSL
* Authentification intégrée
* Mise à l'échelle automatique

---

### Cas d'utilisation

* Applications web
* APIs REST
* Backends mobiles

---

## 4. Azure Functions

Azure Functions est un service **Serverless**.

Le code s'exécute uniquement lorsqu'un événement se produit.

---

### Déclencheurs (Triggers)

* HTTP Request
* Timer
* Blob Storage
* Queue Storage
* Event Grid

---

### Exemple

Lorsqu'une image est déposée dans Blob Storage :

* Azure détecte l'événement
* Une Function est exécutée
* L'image est automatiquement redimensionnée

---

### Avantages

* Paiement à l'exécution
* Pas de serveur à administrer
* Très scalable

---

## 5. Containers

Un conteneur permet d'exécuter une application avec toutes ses dépendances.

L'outil le plus utilisé est Docker.

---

### Avantages

* Léger
* Portable
* Rapide à démarrer

---

### Exemple

Une application Java :

* Application
* JDK
* Bibliothèques

Tout est regroupé dans une seule image Docker.

---

## 6. Azure Container Instances (ACI)

ACI permet d'exécuter un conteneur sans gérer d'infrastructure.

---

### Cas d'utilisation

* Traitements ponctuels
* Tests rapides
* Automatisation

---

### Avantages

* Démarrage rapide
* Pas de cluster à administrer
* Facturation à l'utilisation

---

## 7. Azure Kubernetes Service (AKS)

AKS est le service Kubernetes managé de Microsoft.

Kubernetes permet d'orchestrer plusieurs conteneurs.

---

### Fonctionnalités

* Auto-scaling
* Auto-healing
* Rolling Updates
* Haute disponibilité

---

### Cas d'utilisation

* Microservices
* Applications cloud natives
* Plateformes à grande échelle

---

### Avantages

* Gestion simplifiée de Kubernetes
* Intégration Azure
* Forte scalabilité

---

## 8. Azure Virtual Desktop (AVD)

Azure Virtual Desktop permet d'exécuter des bureaux Windows dans Azure.

Les utilisateurs accèdent à leur environnement depuis n'importe quel appareil.

---

### Cas d'utilisation

* Télétravail
* Sous-traitance
* Postes de travail sécurisés

---

### Avantages

* Gestion centralisée
* Sécurité renforcée
* Réduction des coûts matériels

---

## Comparaison des services Compute

| Service          | Type           | Gestion utilisateur |
| ---------------- | -------------- | ------------------- |
| Virtual Machines | IaaS           | Élevée              |
| VM Scale Sets    | IaaS           | Élevée              |
| App Service      | PaaS           | Faible              |
| Functions        | Serverless     | Très faible         |
| ACI              | Containers     | Faible              |
| AKS              | Kubernetes     | Moyenne             |
| AVD              | Bureau virtuel | Faible              |

---

## Comment choisir ?

### Besoin d'un contrôle total ?

→ Azure Virtual Machines

### Héberger une application web ?

→ Azure App Service

### Exécuter du code à la demande ?

→ Azure Functions

### Lancer rapidement un conteneur ?

→ Azure Container Instances

### Gérer plusieurs conteneurs ?

→ Azure Kubernetes Service

### Fournir un bureau distant ?

→ Azure Virtual Desktop

---

## Résumé

Les principaux services Compute Azure sont :

* Azure Virtual Machines
* Virtual Machine Scale Sets
* Azure App Service
* Azure Functions
* Azure Container Instances
* Azure Kubernetes Service
* Azure Virtual Desktop

Chaque service répond à un besoin spécifique selon le niveau de contrôle et d'administration souhaité.

---

## À retenir pour l'examen AZ-900

* VM = IaaS
* App Service = PaaS
* Functions = Serverless
* ACI = Exécution rapide de conteneurs
* AKS = Kubernetes managé
* VMSS = Auto-scaling des VM
* AVD = Bureau virtuel dans Azure

### Question fréquente AZ-900

**Je veux héberger un site web sans gérer de serveur.**

Réponse : **Azure App Service**

**Je veux exécuter du code uniquement lorsqu'un événement se produit.**

Réponse : **Azure Functions**

**Je veux gérer des microservices conteneurisés à grande échelle.**

Réponse : **Azure Kubernetes Service (AKS)**

**Je veux un contrôle complet sur mon système d'exploitation.**

Réponse : **Azure Virtual Machines**
