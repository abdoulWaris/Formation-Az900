# 10 - Azure Monitoring

## Introduction

Surveiller une infrastructure cloud est essentiel pour garantir la disponibilité, les performances et la sécurité des applications.

Azure fournit plusieurs outils permettant de :

* Surveiller les ressources
* Collecter des métriques
* Centraliser les journaux (logs)
* Détecter les anomalies
* Recevoir des alertes

Pour l'examen AZ-900, il est important de connaître les principaux services de supervision proposés par Azure.

---

## 1. Azure Monitor

Azure Monitor est le service central de supervision d'Azure.

Il collecte et analyse les données provenant des ressources Azure.

---

### Azure Monitor permet de

* Surveiller les performances
* Collecter des métriques
* Collecter les journaux (logs)
* Déclencher des alertes
* Créer des tableaux de bord

---

### Ressources surveillées

* Machines Virtuelles
* Azure App Service
* Azure SQL Database
* Azure Storage
* Azure Kubernetes Service (AKS)

---

## 2. Les Métriques (Metrics)

Les métriques sont des données numériques collectées en temps réel.

---

### Exemples

* Utilisation CPU
* Mémoire
* Nombre de requêtes
* Temps de réponse
* Espace disque

---

### Utilisation

Les métriques permettent de :

* Détecter une surcharge
* Mesurer les performances
* Mettre en place l'Auto-Scaling

---

## 3. Les Journaux (Logs)

Les logs enregistrent les événements produits par les ressources Azure.

---

### Exemples

* Connexions utilisateur
* Erreurs applicatives
* Modifications de configuration
* Événements système

---

### Avantages

* Analyse des incidents
* Audit
* Dépannage

---

## 4. Log Analytics

Log Analytics est un service permettant d'interroger et d'analyser les logs collectés.

---

### Fonctionnalités

* Recherche dans les journaux
* Création de rapports
* Analyse des performances
* Détection d'anomalies

---

### Langage utilisé

Kusto Query Language (KQL)

---

### Exemple de requête

```kusto
AzureActivity
| limit 10
```

Cette requête affiche les 10 derniers événements enregistrés.

---

## 5. Azure Alerts

Azure Alerts permet d'envoyer des notifications lorsqu'une condition est remplie.

---

### Exemples

* CPU supérieur à 80 %
* Stockage presque saturé
* Échec d'une machine virtuelle
* Dépassement d'un budget

---

### Moyens de notification

* E-mail
* SMS
* Notification Push
* Webhook

---

## 6. Action Groups

Les Action Groups définissent les actions à effectuer lorsqu'une alerte est déclenchée.

---

### Exemple

Si le CPU dépasse 90 % :

* Envoyer un e-mail
* Envoyer un SMS
* Déclencher une Azure Function

---

## 7. Application Insights

Application Insights est un service de surveillance des applications.

Il est particulièrement adapté aux applications web et aux API.

---

### Fonctionnalités

* Temps de réponse
* Nombre de requêtes
* Exceptions
* Dépendances
* Disponibilité

---

### Cas d'utilisation

* Détection des erreurs applicatives
* Analyse des performances
* Suivi de l'expérience utilisateur

---

## 8. Service Health

Azure Service Health informe sur l'état des services Azure.

---

### Il permet de connaître

* Les incidents Azure
* Les maintenances planifiées
* Les recommandations

---

### Avantages

* Anticiper les interruptions
* Identifier les problèmes liés à Azure

---

## 9. Resource Health

Resource Health indique l'état d'une ressource Azure spécifique.

---

### États possibles

* Available
* Unavailable
* Degraded
* Unknown

---

### Exemple

Une VM ne démarre plus.

Resource Health permet de savoir si le problème provient :

* De la VM
* De l'infrastructure Azure

---

## 10. Azure Advisor

Azure Advisor fournit des recommandations personnalisées pour améliorer votre environnement Azure.

---

### Domaines couverts

* Fiabilité
* Sécurité
* Performance
* Coûts
* Excellence opérationnelle

---

### Exemple

Azure Advisor peut recommander :

* Redimensionner une VM surdimensionnée
* Activer des sauvegardes
* Supprimer des ressources inutilisées

---

## Architecture de Supervision

```text
Application Azure
        │
        ▼
Azure Monitor
        │
 ┌──────┴─────────┐
 ▼                ▼
Metrics         Logs
 │                │
 ▼                ▼
Alerts      Log Analytics
        │
        ▼
 Action Groups
        │
        ▼
Notifications
```

---

## Comparaison des Services

| Service              | Rôle                           |
| -------------------- | ------------------------------ |
| Azure Monitor        | Supervision globale            |
| Metrics              | Mesures en temps réel          |
| Logs                 | Événements détaillés           |
| Log Analytics        | Analyse des journaux           |
| Alerts               | Notifications                  |
| Action Groups        | Actions suite aux alertes      |
| Application Insights | Surveillance des applications  |
| Service Health       | État des services Azure        |
| Resource Health      | État d'une ressource           |
| Azure Advisor        | Recommandations d'optimisation |

---

## Exemple Concret

Une application web est hébergée sur Azure App Service.

Vous souhaitez :

* Surveiller son temps de réponse
* Être alerté si le CPU dépasse 80 %
* Analyser les erreurs
* Vérifier la disponibilité du service

Services utilisés :

* Azure Monitor
* Metrics
* Alerts
* Action Groups
* Application Insights

---

## Résumé

Azure Monitoring permet de surveiller les performances, la disponibilité et la santé des ressources Azure.

Les principaux services sont :

* Azure Monitor
* Log Analytics
* Application Insights
* Azure Alerts
* Azure Advisor
* Service Health
* Resource Health

Ils permettent d'améliorer la fiabilité, d'anticiper les incidents et d'optimiser les performances.

---

## À retenir pour l'examen AZ-900

### Supervision

* Azure Monitor = service central de monitoring
* Metrics = données numériques
* Logs = événements détaillés

### Analyse

* Log Analytics = requêtes KQL
* Application Insights = surveillance des applications

### Notifications

* Alerts = détection d'événements
* Action Groups = actions automatiques

### Santé des services

* Service Health = état des services Azure
* Resource Health = état d'une ressource

### Optimisation

* Azure Advisor = recommandations personnalisées

---

## Questions fréquentes AZ-900

**Je veux surveiller toutes mes ressources Azure**

→ Azure Monitor

**Je veux analyser les journaux d'une application**

→ Log Analytics

**Je veux surveiller les performances d'une API**

→ Application Insights

**Je veux recevoir un e-mail lorsque le CPU dépasse 80 %**

→ Azure Alerts + Action Groups

**Je veux savoir si une panne provient d'Azure**

→ Service Health

**Je veux connaître l'état d'une machine virtuelle spécifique**

→ Resource Health

**Je veux obtenir des recommandations pour améliorer les performances et réduire les coûts**

→ Azure Advisor
