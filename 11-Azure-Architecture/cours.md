# 11 - Azure High Availability, Scalability & Reliability

## Introduction

L'un des principaux avantages du cloud est de proposer des services **hautement disponibles**, **évolutifs** et **résilients**.

Azure fournit plusieurs mécanismes permettant de garantir que les applications restent accessibles même en cas de panne ou de forte augmentation du trafic.

Ces notions sont très présentes dans l'examen **AZ-900**.

---

## 1. High Availability (Haute Disponibilité)

La haute disponibilité (High Availability ou HA) désigne la capacité d'un service à rester disponible malgré une panne.

L'objectif est de limiter les interruptions de service.

---

### Comment Azure assure la haute disponibilité ?

* Plusieurs centres de données
* Availability Zones
* Load Balancer
* Réplication des données
* Redondance des ressources

---

### Exemple

Une machine virtuelle tombe en panne.

Une seconde VM prend automatiquement le relais.

Les utilisateurs ne remarquent pas l'interruption.

---

## 2. Fault Tolerance (Tolérance aux Pannes)

La tolérance aux pannes est la capacité d'un système à continuer de fonctionner malgré la défaillance d'un composant.

---

### Exemple

Une alimentation électrique d'un datacenter tombe en panne.

Les autres composants continuent d'assurer le fonctionnement du service.

---

### Objectif

Éviter l'arrêt complet d'une application.

---

## 3. Scalability (Scalabilité)

La scalabilité est la capacité d'augmenter ou de réduire les ressources selon les besoins.

---

### Vertical Scaling (Scale Up)

Augmenter les ressources d'une seule machine.

Exemples :

* Plus de CPU
* Plus de RAM
* Plus de stockage

---

### Horizontal Scaling (Scale Out)

Ajouter plusieurs instances d'une application.

Exemple :

* 1 VM → 5 VM

Le trafic est réparti grâce à un Load Balancer.

---

### Comparaison

| Verticale         | Horizontale      |
| ----------------- | ---------------- |
| Plus de puissance | Plus de machines |
| Limite matérielle | Très scalable    |
| Plus simple       | Plus résiliente  |

---

## 4. Elasticity (Élasticité)

L'élasticité permet d'ajuster automatiquement les ressources en fonction de la charge.

Contrairement à la scalabilité, l'élasticité est **automatique**.

---

### Exemple

Le trafic augmente :

* Azure ajoute automatiquement des VM.

Le trafic diminue :

* Azure supprime les VM inutiles.

---

### Avantages

* Optimisation des coûts
* Adaptation en temps réel
* Meilleures performances

---

## 5. Load Balancer

Azure Load Balancer répartit le trafic entre plusieurs ressources.

---

### Avantages

* Haute disponibilité
* Répartition de charge
* Meilleures performances

---

### Exemple

```text
Utilisateurs
      │
      ▼
Load Balancer
   ┌──┴──┐
   ▼     ▼
 VM1   VM2
```

---

## 6. Availability Zones

Les Availability Zones sont des centres de données physiquement séparés dans une même région Azure.

Chaque zone possède :

* Une alimentation indépendante
* Un système de refroidissement indépendant
* Un réseau indépendant

---

### Avantages

* Protection contre les pannes locales
* Haute disponibilité
* Réduction des interruptions

---

## 7. Region Pairs

Azure associe certaines régions par paires.

Exemples :

* France Central ↔ France South
* North Europe ↔ West Europe

---

### Avantages

* Réplication des données
* Reprise après sinistre
* Continuité des activités

---

## 8. Disaster Recovery (Reprise après Sinistre)

Le Disaster Recovery permet de restaurer un service après une catastrophe majeure.

---

### Exemples

* Incendie d'un datacenter
* Inondation
* Panne régionale

---

### Solutions Azure

* Azure Site Recovery
* Geo-Redundant Storage (GRS)

---

## 9. Azure Backup

Azure Backup est un service de sauvegarde managé.

---

### Fonctionnalités

* Sauvegardes automatiques
* Chiffrement
* Restauration rapide

---

### Ressources compatibles

* Machines virtuelles
* Bases de données
* Fichiers

---

## 10. Azure Site Recovery

Azure Site Recovery (ASR) permet de répliquer les machines virtuelles vers une autre région.

En cas de panne majeure, les applications peuvent être redémarrées rapidement.

---

### Avantages

* Réduction du temps d'interruption
* Continuité des activités
* Reprise automatisée

---

## 11. Service Level Agreement (SLA)

Un SLA (Service Level Agreement) est un engagement de Microsoft concernant la disponibilité d'un service.

Il est exprimé en pourcentage.

---

### Exemples

| SLA      | Disponibilité                 |
| -------- | ----------------------------- |
| 99 %     | Environ 3,65 jours d'arrêt/an |
| 99,9 %   | Environ 8,8 heures d'arrêt/an |
| 99,99 %  | Environ 52 minutes d'arrêt/an |
| 99,999 % | Environ 5 minutes d'arrêt/an  |

---

### Important

Plus le pourcentage est élevé, moins le temps d'arrêt autorisé est important.

---

## 12. Business Continuity

La continuité d'activité (Business Continuity) regroupe les stratégies permettant à une entreprise de continuer à fonctionner malgré un incident.

Elle s'appuie sur :

* Sauvegardes
* Réplication
* Haute disponibilité
* Reprise après sinistre

---

## Architecture Résiliente Azure

```text
                Utilisateurs
                      │
                      ▼
              Azure Load Balancer
                ┌─────────────┐
                ▼             ▼
          VM Zone 1      VM Zone 2
                │             │
                └──────┬──────┘
                       ▼
              Azure SQL Database
                       │
              Sauvegarde + GRS
                       │
                Région secondaire
```

---

## Résumé

Azure garantit la disponibilité et la résilience des applications grâce à :

* Availability Zones
* Region Pairs
* Load Balancer
* Auto Scaling
* Azure Backup
* Azure Site Recovery

Ces mécanismes permettent de réduire les interruptions de service et d'assurer la continuité des activités.

---

## À retenir pour l'examen AZ-900

### Disponibilité

* High Availability = service toujours accessible
* Fault Tolerance = fonctionnement malgré une panne

### Scalabilité

* Scale Up = ajouter des ressources à une VM
* Scale Out = ajouter plusieurs VM

### Élasticité

* Ajustement automatique des ressources selon la demande

### Continuité

* Azure Backup = sauvegarde
* Azure Site Recovery = reprise après sinistre
* Region Pairs = réplication entre régions

### SLA

* Engagement de disponibilité de Microsoft
* Plus le SLA est élevé, plus le temps d'arrêt autorisé est faible

---

## Questions fréquentes AZ-900

**Je veux augmenter la puissance d'une VM existante**

→ Vertical Scaling (Scale Up)

**Je veux ajouter plusieurs serveurs pour absorber plus de trafic**

→ Horizontal Scaling (Scale Out)

**Je veux que les ressources s'adaptent automatiquement à la charge**

→ Elasticity

**Je veux répartir le trafic entre plusieurs serveurs**

→ Azure Load Balancer

**Je veux sauvegarder mes machines virtuelles**

→ Azure Backup

**Je veux redémarrer mes applications dans une autre région en cas de catastrophe**

→ Azure Site Recovery

**Je veux connaître le niveau de disponibilité garanti par Microsoft**

→ Service Level Agreement (SLA)

