# 09 - Azure Cost Management

## Introduction

L'un des principaux avantages du cloud est le modèle **Pay-As-You-Go** : vous payez uniquement pour les ressources que vous utilisez.

Azure fournit plusieurs outils permettant :

* D'estimer les coûts
* De surveiller les dépenses
* D'optimiser les ressources
* De contrôler les budgets

La gestion des coûts est une compétence importante pour l'examen AZ-900.

---

## 1. Le Modèle Pay-As-You-Go

Dans Azure, la plupart des services sont facturés selon leur consommation.

---

### Exemples

#### Machine Virtuelle

Facturation selon :

* Le type de VM
* Le nombre d'heures utilisées

---

#### Stockage

Facturation selon :

* Le volume stocké
* Les transferts de données
* Les opérations effectuées

---

#### Azure Functions

Facturation selon :

* Le nombre d'exécutions
* Le temps d'exécution

---

### Avantages

* Pas d'investissement initial
* Paiement à l'usage
* Flexibilité

---

## 2. Facteurs Influençant le Coût

Plusieurs éléments impactent le prix d'un service Azure.

---

### Type de ressource

Exemple :

* Une VM Standard coûte moins cher qu'une VM Premium.

---

### Région

Les prix peuvent varier selon la région Azure utilisée.

Exemples :

* France Central
* West Europe
* East US

---

### Consommation

Plus une ressource est utilisée, plus son coût augmente.

---

### Trafic réseau

Les transferts de données sortants peuvent être facturés.

---

## 3. Azure Pricing Calculator

Azure Pricing Calculator permet d'estimer le coût d'une solution avant son déploiement.

---

### Fonctionnalités

* Calcul prévisionnel
* Comparaison de services
* Simulation d'architectures

---

### Cas d'utilisation

Avant un projet :

* VM
* Stockage
* Base de données

Vous pouvez estimer le coût mensuel.

---

## 4. Total Cost of Ownership (TCO) Calculator

Le TCO Calculator aide à comparer :

* Une infrastructure locale (On-Premise)
* Une infrastructure Azure

---

### Prend en compte

* Serveurs
* Réseau
* Électricité
* Maintenance
* Licences

---

### Objectif

Mesurer les économies potentielles lors d'une migration vers Azure.

---

## 5. Azure Cost Management

Azure Cost Management permet de surveiller et d'analyser les dépenses Azure.

---

### Fonctionnalités

* Analyse des coûts
* Rapports détaillés
* Prévisions budgétaires
* Alertes

---

### Avantages

* Contrôle des dépenses
* Visibilité complète
* Optimisation financière

---

## 6. Budgets

Les budgets permettent de définir des limites de dépenses.

---

### Exemple

Budget mensuel :

* 500 €

Lorsque 80 % du budget est atteint :

* Notification automatique

---

### Avantages

* Prévention des dépassements
* Contrôle financier

---

## 7. Alerts (Alertes)

Les alertes notifient les administrateurs lorsqu'un seuil est dépassé.

---

### Exemples

* Budget dépassé
* Consommation anormale
* Hausse soudaine des coûts

---

## 8. Tags pour le Suivi des Coûts

Les Tags permettent de catégoriser les ressources.

---

### Exemple

```text
Environment = Production
Department = Marketing
Project = SupMap
```

---

### Avantages

* Répartition des coûts
* Analyse par équipe
* Facturation interne

---

## 9. Réservation de Ressources (Reserved Instances)

Azure permet de réserver certaines ressources sur :

* 1 an
* 3 ans

---

### Avantages

* Réduction importante des coûts
* Tarifs prévisibles

---

### Cas d'utilisation

Ressources utilisées en permanence :

* VM de production
* Bases de données critiques

---

## 10. Spot Virtual Machines

Les Spot VMs utilisent les capacités inutilisées des datacenters Azure.

---

### Avantages

* Très faible coût

---

### Limitation

Microsoft peut interrompre la VM à tout moment.

---

### Cas d'utilisation

* Tests
* Calculs temporaires
* Traitements non critiques

---

## 11. Bonnes Pratiques d'Optimisation

### Supprimer les ressources inutilisées

Exemples :

* VM arrêtées
* Disques non utilisés
* IP publiques inutiles

---

### Utiliser l'Auto-Scaling

Adapter automatiquement les ressources à la demande.

---

### Choisir le bon niveau de stockage

* Hot
* Cool
* Archive

---

### Utiliser les Reserved Instances

Pour les charges de travail stables.

---

### Surveiller régulièrement les coûts

Grâce à Azure Cost Management.

---

## Outils de Gestion des Coûts

| Outil              | Fonction                       |
| ------------------ | ------------------------------ |
| Pricing Calculator | Estimation des coûts           |
| TCO Calculator     | Comparaison On-Premise / Azure |
| Cost Management    | Analyse des dépenses           |
| Budgets            | Limitation des coûts           |
| Alerts             | Notifications                  |
| Tags               | Répartition des coûts          |

---

## Exemple Concret

Une entreprise déploie :

* 5 VM
* Azure SQL Database
* Blob Storage

Avant le déploiement :

1. Estimation via Pricing Calculator
2. Définition d'un budget
3. Configuration des alertes
4. Attribution de Tags

Résultat :

* Coûts maîtrisés
* Suivi facilité
* Réduction des risques financiers

---

## Résumé

Azure propose plusieurs outils permettant de gérer efficacement les dépenses cloud :

* Pricing Calculator
* TCO Calculator
* Azure Cost Management
* Budgets
* Alerts
* Tags

Ces outils aident à optimiser les ressources et à éviter les dépassements de budget.

---

## À retenir pour l'examen AZ-900

### Estimation

* Pricing Calculator
* TCO Calculator

### Suivi

* Azure Cost Management
* Budgets
* Alerts

### Optimisation

* Reserved Instances
* Spot Virtual Machines
* Auto-Scaling

### Organisation

* Tags

---

## Questions fréquentes AZ-900

**Je veux estimer le coût d'une architecture Azure avant son déploiement**

→ Azure Pricing Calculator

**Je veux comparer mon datacenter actuel avec Azure**

→ TCO Calculator

**Je veux surveiller les dépenses de mon abonnement**

→ Azure Cost Management

**Je veux recevoir une alerte lorsque je dépasse un budget**

→ Budgets + Alerts

**Je veux réduire le coût d'une VM utilisée en permanence**

→ Reserved Instance

**Je veux utiliser des ressources Azure à très faible coût pour des traitements non critiques**

→ Spot Virtual Machine
