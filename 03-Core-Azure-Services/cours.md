# 03 - Core Azure Services

## Introduction

Microsoft Azure propose plus de 200 services cloud permettant aux entreprises de développer, déployer et gérer des applications à l'échelle mondiale.

Pour l'examen AZ-900, il n'est pas nécessaire de connaître tous les services Azure. Il faut surtout comprendre les principaux services et savoir dans quels cas les utiliser.

---

## 1. Catégories principales de services Azure

Les services Azure peuvent être regroupés en plusieurs grandes catégories :

* Compute
* Networking
* Storage
* Databases
* Security
* Analytics & AI

---

## 2. Services de Calcul (Compute)

Les services Compute permettent d'exécuter des applications, des conteneurs ou des machines virtuelles.

### Azure Virtual Machines (VM)

Les Virtual Machines permettent de créer des serveurs Windows ou Linux dans Azure.

#### Cas d'utilisation

* Héberger une application web
* Exécuter un serveur d'entreprise
* Migrer une application existante vers Azure

#### Avantages

* Contrôle total du système d'exploitation
* Grande flexibilité
* Compatible avec de nombreux logiciels

---

### Azure App Service

Azure App Service est une plateforme permettant d'héberger des applications web sans gérer l'infrastructure.

#### Langages supportés

* Java
* .NET
* Python
* Node.js
* PHP

#### Avantages

* Déploiement rapide
* Maintenance simplifiée
* Mise à l'échelle automatique

---

### Azure Functions

Azure Functions permet d'exécuter du code en mode Serverless.

Le code est déclenché uniquement lorsqu'un événement se produit.

#### Exemples

* Réception d'une requête HTTP
* Ajout d'un fichier dans un stockage
* Exécution planifiée

#### Avantages

* Paiement uniquement à l'utilisation
* Aucun serveur à gérer

---

### Azure Kubernetes Service (AKS)

AKS est le service Kubernetes managé d'Azure.

Il permet de déployer et gérer des conteneurs à grande échelle.

#### Avantages

* Orchestration automatique
* Mise à l'échelle simplifiée
* Haute disponibilité

---

## 3. Services de Stockage

Azure Storage permet de stocker des données de manière sécurisée et durable.

---

### Azure Blob Storage

Service de stockage d'objets.

#### Exemples de fichiers

* Images
* Vidéos
* Documents PDF
* Sauvegardes

#### Cas d'utilisation

* Stockage de médias
* Archivage
* Sauvegarde de données

---

### Azure Files

Partage de fichiers dans le cloud.

Compatible avec le protocole SMB utilisé par Windows.

#### Cas d'utilisation

* Partage de fichiers entre utilisateurs
* Migration de serveurs de fichiers

---

## 4. Services de Base de Données

Azure propose plusieurs solutions de bases de données.

---

### Azure SQL Database

Base de données relationnelle basée sur Microsoft SQL Server.

#### Caractéristiques

* Sauvegardes automatiques
* Haute disponibilité
* Sécurité intégrée

#### Cas d'utilisation

* Applications métier
* Applications web

---

### Azure Cosmos DB

Base de données NoSQL distribuée mondialement.

#### Avantages

* Très faible latence
* Réplication mondiale
* Forte scalabilité

#### Cas d'utilisation

* Réseaux sociaux
* Applications mobiles
* Jeux en ligne

---

## 5. Services Réseau

Azure fournit plusieurs services permettant de connecter les ressources.

### Azure Virtual Network (VNet)

Permet de créer un réseau privé dans Azure.

Comparable à un réseau d'entreprise traditionnel.

---

### VPN Gateway

Permet de connecter un réseau local à Azure via Internet de manière sécurisée.

---

### ExpressRoute

Connexion privée entre Azure et un datacenter d'entreprise.

#### Avantages

* Plus rapide
* Plus sécurisé
* Latence réduite

---

## 6. Services d'Intelligence Artificielle

Azure propose plusieurs services d'IA prêts à l'emploi.

### Azure AI Services

Permet d'ajouter facilement de l'intelligence artificielle à une application.

#### Fonctionnalités

* Reconnaissance d'images
* Traduction
* Analyse de texte
* Synthèse vocale

---

## 7. Azure Marketplace

Azure Marketplace est une boutique permettant de déployer rapidement des solutions préconfigurées.

Exemples :

* Machines virtuelles
* Bases de données
* Solutions de sécurité
* Outils DevOps

---

## Résumé

Les principaux services Azure à connaître pour AZ-900 sont :

### Compute

* Azure Virtual Machines
* Azure App Service
* Azure Functions
* Azure Kubernetes Service (AKS)

### Storage

* Azure Blob Storage
* Azure Files

### Databases

* Azure SQL Database
* Azure Cosmos DB

### Networking

* Azure Virtual Network
* VPN Gateway
* ExpressRoute

### AI

* Azure AI Services

---

## À retenir pour l'examen AZ-900

* VM = Infrastructure as a Service (IaaS)
* App Service = Platform as a Service (PaaS)
* Functions = Serverless
* AKS = Kubernetes managé
* Blob Storage = stockage d'objets
* Azure Files = partage de fichiers
* Azure SQL Database = base relationnelle
* Cosmos DB = base NoSQL
* VNet = réseau privé Azure
* ExpressRoute = connexion privée vers Azure
* Azure AI Services = services d'intelligence artificielle prêts à l'emploi
