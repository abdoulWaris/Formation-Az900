# 06 - Azure Storage

## Introduction

Le stockage est l'un des services fondamentaux d'Azure.

Azure Storage permet de stocker des données de manière :

* Sécurisée
* Durable
* Hautement disponible
* Scalable

Les données peuvent être stockées sous différentes formes selon les besoins de l'application.

---

## 1. Azure Storage Account

Un Storage Account est le conteneur principal qui héberge les services de stockage Azure.

Toutes les données sont stockées à l'intérieur d'un compte de stockage.

---

### Types de données supportés

* Blob Storage
* Azure Files
* Queue Storage
* Table Storage

---

## 2. Azure Blob Storage

Blob Storage est un service de stockage d'objets.

Il est utilisé pour stocker de grandes quantités de données non structurées.

---

### Exemples

* Images
* Vidéos
* Documents PDF
* Sauvegardes
* Logs

---

### Cas d'utilisation

* Hébergement de fichiers statiques
* Archivage
* Data Lake
* Sauvegardes

---

### Structure

Storage Account
└── Container
└── Blob

---

## 3. Azure Files

Azure Files fournit des partages de fichiers accessibles via le protocole SMB.

---

### Cas d'utilisation

* Remplacement de serveurs de fichiers
* Partage de documents
* Applications nécessitant un stockage partagé

---

### Avantages

* Compatible Windows, Linux et macOS
* Accessible depuis Azure et on-premise

---

## 4. Azure Queue Storage

Queue Storage permet d'échanger des messages entre applications.

---

### Cas d'utilisation

* Communication asynchrone
* Traitements distribués
* Découplage des applications

---

### Exemple

Application Web
↓
Queue Storage
↓
Worker Service

---

## 5. Azure Table Storage

Table Storage est une base de données NoSQL simple.

---

### Caractéristiques

* Stockage de données structurées
* Très scalable
* Coût faible

---

### Cas d'utilisation

* Journaux applicatifs
* Métadonnées
* Applications simples

---

## 6. Azure Disk Storage

Azure Disk Storage fournit des disques persistants pour les machines virtuelles.

---

### Types de disques

#### Standard HDD

* Faible coût
* Performance modérée

---

#### Standard SSD

* Bon compromis coût/performance

---

#### Premium SSD

* Haute performance
* Applications critiques

---

## 7. Redondance des données

Azure réplique automatiquement les données afin de garantir leur disponibilité.

---

### LRS (Locally Redundant Storage)

3 copies dans un même datacenter.

---

### ZRS (Zone-Redundant Storage)

3 copies réparties dans plusieurs zones de disponibilité.

---

### GRS (Geo-Redundant Storage)

Les données sont répliquées dans une autre région Azure.

---

### RA-GRS (Read Access Geo-Redundant Storage)

Même principe que GRS avec accès en lecture à la région secondaire.

---

## Comparaison

| Type   | Protection                   |
| ------ | ---------------------------- |
| LRS    | Datacenter                   |
| ZRS    | Zones                        |
| GRS    | Régions                      |
| RA-GRS | Régions + Lecture secondaire |

---

## 8. Niveaux d'accès (Access Tiers)

Azure Blob Storage propose plusieurs niveaux de stockage.

---

### Hot Tier

Pour les données fréquemment consultées.

Exemples :

* Site web
* Images utilisées régulièrement

---

### Cool Tier

Pour les données peu consultées.

Exemples :

* Sauvegardes récentes
* Archives temporaires

---

### Archive Tier

Pour les données rarement consultées.

Exemples :

* Archives légales
* Données historiques

---

## Comparaison

| Tier    | Coût stockage | Coût accès |
| ------- | ------------- | ---------- |
| Hot     | Élevé         | Faible     |
| Cool    | Moyen         | Moyen      |
| Archive | Très faible   | Élevé      |

---

## 9. Azure Storage Explorer

Azure Storage Explorer est un outil graphique permettant de gérer les données Azure Storage.

---

### Fonctionnalités

* Téléverser des fichiers
* Télécharger des fichiers
* Gérer les conteneurs Blob
* Administrer les partages Azure Files

---

## 10. Sécurité du stockage

Azure Storage intègre plusieurs mécanismes de sécurité.

---

### Chiffrement au repos

Les données sont automatiquement chiffrées lorsqu'elles sont stockées.

---

### Chiffrement en transit

Les communications utilisent HTTPS/TLS.

---

### Shared Access Signature (SAS)

Permet de donner un accès temporaire à une ressource.

---

### Contrôle d'accès via Azure AD

Gestion des permissions basée sur les identités.

---

## Architecture de stockage typique

Application Web
↓
Azure Blob Storage

Machine Virtuelle
↓
Azure Disk Storage

Applications distribuées
↓
Azure Queue Storage

Partage de documents
↓
Azure Files

---

## Résumé

Azure Storage propose plusieurs solutions adaptées à différents besoins :

* Blob Storage → objets
* Azure Files → partage de fichiers
* Queue Storage → messages
* Table Storage → NoSQL simple
* Disk Storage → stockage des VM

Azure garantit également la disponibilité des données grâce à différents niveaux de redondance.

---

## À retenir pour l'examen AZ-900

* Storage Account = conteneur principal
* Blob Storage = stockage d'objets
* Azure Files = partage de fichiers SMB
* Queue Storage = messagerie
* Table Storage = NoSQL
* Disk Storage = disques des VM

### Redondance

* LRS = même datacenter
* ZRS = plusieurs zones
* GRS = autre région
* RA-GRS = autre région avec lecture

### Access Tiers

* Hot = accès fréquent
* Cool = accès occasionnel
* Archive = archivage long terme

---

## Questions fréquentes AZ-900

**Je veux stocker des images et des vidéos**

→ Azure Blob Storage

**Je veux partager des fichiers comme un serveur Windows**

→ Azure Files

**Je veux échanger des messages entre applications**

→ Azure Queue Storage

**Je veux un disque pour une machine virtuelle**

→ Azure Disk Storage

**Je veux conserver des données pendant plusieurs années au moindre coût**

→ Archive Tier

**Je veux protéger mes données contre une panne régionale**

→ GRS ou RA-GRS
