# 05 - Azure Networking

## Introduction

Les services réseau (Networking) dans Azure permettent de connecter les ressources entre elles, de sécuriser les communications et de gérer le trafic entrant et sortant.

Azure Networking est essentiel pour construire des applications cloud sécurisées, performantes et scalables.

---

## 1. Virtual Network (VNet)

Une Virtual Network (VNet) est un réseau privé dans Azure.

Elle permet aux ressources Azure (VM, bases de données, services) de communiquer entre elles de manière sécurisée.

---

### Caractéristiques

* Isolation réseau
* Communication entre ressources Azure
* Connexion avec Internet ou réseaux locaux

---

### Cas d'utilisation

* Héberger une architecture applicative complète
* Séparer frontend et backend
* Sécuriser les échanges entre services

---

## 2. Subnets

Un subnet est une subdivision logique d'un Virtual Network.

---

### Exemple

VNet :

* Frontend subnet
* Backend subnet
* Database subnet

---

### Avantages

* Organisation des ressources
* Séparation des responsabilités
* Amélioration de la sécurité

---

## 3. Network Security Groups (NSG)

Un NSG est un pare-feu réseau permettant de contrôler le trafic entrant et sortant.

---

### Règles NSG

* Autoriser ou bloquer du trafic
* Basé sur :

  * IP source
  * Port
  * Protocole

---

### Exemple

* Autoriser HTTP (port 80)
* Bloquer SSH depuis Internet
* Autoriser uniquement le réseau interne

---

## 4. Application Security Groups (ASG)

Les ASG permettent de regrouper des machines virtuelles pour simplifier les règles de sécurité.

---

### Avantages

* Gestion simplifiée
* Moins de règles NSG complexes
* Sécurité basée sur les applications

---

## 5. VPN Gateway

VPN Gateway permet de connecter un réseau local (on-premise) à Azure via une connexion sécurisée sur Internet.

---

### Cas d'utilisation

* Extension d'un réseau d'entreprise vers Azure
* Accès sécurisé aux ressources cloud

---

### Avantages

* Connexion sécurisée
* Chiffrement des données
* Mise en place rapide

---

## 6. ExpressRoute

ExpressRoute est une connexion privée entre un datacenter et Azure.

---

### Différence avec VPN

| VPN Gateway      | ExpressRoute     |
| ---------------- | ---------------- |
| Internet         | Connexion privée |
| Moins cher       | Plus coûteux     |
| Moins performant | Très performant  |

---

### Avantages

* Latence faible
* Sécurité élevée
* Connexion stable

---

## 7. Azure Load Balancer

Le Load Balancer distribue le trafic entre plusieurs ressources backend.

---

### Types

* Public Load Balancer
* Internal Load Balancer

---

### Avantages

* Haute disponibilité
* Répartition de charge
* Amélioration des performances

---

## 8. Application Gateway

Application Gateway est un Load Balancer au niveau HTTP/HTTPS (Layer 7).

---

### Fonctionnalités

* Routage basé sur URL
* SSL termination
* Web Application Firewall (WAF)

---

## 9. Azure DNS

Azure DNS permet de gérer les noms de domaine.

---

### Exemple

* [www.monapp.com](http://www.monapp.com) → Azure App Service
* api.monapp.com → Azure Function

---

## 10. Content Delivery Network (CDN)

CDN permet de distribuer du contenu plus rapidement en le mettant en cache dans des serveurs proches des utilisateurs.

---

### Cas d'utilisation

* Sites web
* Vidéos
* Images

---

### Avantages

* Réduction de latence
* Amélioration des performances
* Expérience utilisateur optimisée

---

## 11. Traffic Manager

Traffic Manager est un système de routage global basé sur DNS.

---

### Méthodes de routage

* Priority
* Performance
* Geographic
* Weighted

---

### Cas d'utilisation

* Redirection vers la région la plus proche
* Haute disponibilité globale

---

## Comparaison des services réseau

| Service             | Rôle                             |
| ------------------- | -------------------------------- |
| VNet                | Réseau privé                     |
| Subnet              | Sous-réseau                      |
| NSG                 | Pare-feu                         |
| VPN Gateway         | Connexion sécurisée via Internet |
| ExpressRoute        | Connexion privée dédiée          |
| Load Balancer       | Répartition de charge            |
| Application Gateway | Routing HTTP/HTTPS               |
| CDN                 | Cache global                     |
| Traffic Manager     | Routage global DNS               |

---

## Architecture type Azure Networking

Une application Azure typique peut inclure :

* VNet
* Subnets (frontend/backend)
* NSG pour sécuriser les flux
* Load Balancer pour répartir la charge
* Application Gateway pour le trafic web
* CDN pour améliorer la performance globale

---

## Résumé

Azure Networking permet de :

* Connecter les ressources
* Sécuriser les communications
* Optimiser les performances
* Gérer le trafic global

---

## À retenir pour l'examen AZ-900

* VNet = réseau privé Azure
* Subnet = segmentation du réseau
* NSG = pare-feu
* VPN Gateway = connexion sécurisée via Internet
* ExpressRoute = connexion privée dédiée
* Load Balancer = distribution de trafic
* Application Gateway = routage HTTP/HTTPS
* CDN = contenu distribué globalement
* Traffic Manager = routage global basé DNS

---

## Question fréquente AZ-900

**Je veux sécuriser les communications entre mes VM dans Azure**

→ NSG

**Je veux connecter mon entreprise à Azure de manière sécurisée via Internet**

→ VPN Gateway

**Je veux une connexion privée et très rapide vers Azure**

→ ExpressRoute

**Je veux répartir le trafic entre plusieurs serveurs**

→ Load Balancer

**Je veux améliorer la vitesse de mon site web mondialement**

→ CDN
