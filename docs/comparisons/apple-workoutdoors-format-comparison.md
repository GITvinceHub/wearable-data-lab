# Comparaison des formats d’activités incluant WorkoutDoors  
## Amélioration des exports Apple (HealthKit)

Ce document compare les formats et solutions d’export d’activités sportives en intégrant :contentReference[oaicite:0]{index=0}, afin de montrer comment améliorer significativement l’exploitation des données issues de :contentReference[oaicite:1]{index=1}.

---

## Objectif

L’écosystème Apple produit des données riches mais peu accessibles en formats standards.  
L’utilisation d’une application intermédiaire permet de :

- convertir les données Apple vers des formats interopérables  
- conserver un maximum d’information  
- améliorer les workflows d’analyse  

---

## Vue d’ensemble

| Critère | Apple (Workout / HealthKit) | WorkoutDoors | FIT (Garmin) | TCX | GPX |
|--------|----------------------------|--------------|--------------|-----|-----|
| Format natif | Base HealthKit (DB + XML export) | Interne + export multi-format | FIT (binaire) | XML | XML |
| Export direct GPX | ❌ | ✔️ | ✔️ | ❌ | ✔️ |
| Export TCX | ❌ | ✔️ | ✔️ | ✔️ | ❌ |
| Export FIT | ❌ | ✔️ | ✔️ | ❌ | ❌ |
| Facilité d’export | Faible | Élevée | Élevée | Moyenne | Élevée |

---

## Données GPS et cartographie

| Donnée | Apple | WorkoutDoors | FIT | TCX | GPX |
|--------|------|--------------|-----|-----|-----|
| Trace GPS | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| Altitude | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| Navigation / parcours | ⚠️ | ✔️ (très avancé) | ✔️ | ❌ | ✔️ |
| Cartographie offline | ❌ | ✔️ | ❌ | ❌ | ❌ |

---

## Données sportives

| Donnée | Apple | WorkoutDoors | FIT | TCX | GPX |
|--------|------|--------------|-----|-----|-----|
| Fréquence cardiaque | ✔️ | ✔️ | ✔️ | ✔️ | ⚠️ |
| Cadence | ✔️ | ✔️ | ✔️ | ✔️ | ⚠️ |
| Puissance | ⚠️ | ✔️ | ✔️ | ⚠️ | ⚠️ |
| Calories | ✔️ | ✔️ | ✔️ | ✔️ | ❌ |
| Vitesse / allure | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |

---

## Données avancées

| Donnée | Apple | WorkoutDoors | FIT | TCX | GPX |
|--------|------|--------------|-----|-----|-----|
| Laps / splits | ✔️ | ✔️ | ✔️ | ✔️ | ❌ |
| Zones (FC, puissance) | ✔️ | ✔️ | ✔️ | ❌ | ❌ |
| Running dynamics | ❌ | ⚠️ | ✔️ | ❌ | ❌ |
| Multi-sport | ✔️ | ✔️ | ✔️ | ⚠️ | ❌ |
| Capteurs externes | ✔️ | ✔️ | ✔️ | ❌ | ❌ |

---

## Structure et exploitation

| Critère | Apple | WorkoutDoors | FIT | TCX | GPX |
|--------|------|--------------|-----|-----|-----|
| Lisible humainement | ❌ | ✔️ (exports) | ❌ | ✔️ | ✔️ |
| Standard ouvert | ❌ | ✔️ (exports) | ❌ | ❌ | ✔️ |
| Facilité d’analyse | Faible | Élevée | Moyenne | Élevée | Élevée |
| Perte de données à l’export | N/A | Faible (selon format) | N/A | Moyenne | Élevée |

---

## Rôle spécifique de WorkoutDoors

:contentReference[oaicite:2]{index=2} agit comme une **couche intermédiaire clé** :

### Fonctionnement

- Accès aux données Apple via HealthKit  
- Enrichissement fonctionnel  
- Export vers formats standards  

### Capacités ajoutées

- cartographie détaillée  
- navigation GPX  
- gestion avancée des capteurs  
- structuration des données pour analyse  

### Formats exportés

- **FIT** (équivalent Garmin)  
- **TCX**  
- **GPX**

➡️ Transforme un écosystème Apple fermé en système interopérable

---

## Synthèse opérationnelle

| Objectif | Solution recommandée |
|----------|---------------------|
| Analyse complète | FIT via WorkoutDoors |
| Compatibilité logiciels sportifs | TCX |
| Cartographie / partage | GPX |
| Usage Apple natif | HealthKit (limité) |

---

## Point clé

### Sans WorkoutDoors

- Apple = données riches mais difficilement exploitables  
- Export limité (XML non structuré pour le sport)  

### Avec WorkoutDoors

- Apple → export FIT / TCX / GPX  
- Données exploitables dans tout l’écosystème sport  
- Niveau proche d’un environnement Garmin  

---

## Conclusion

- Apple seul : excellent pour **collecter** des données  
- Limité pour **exporter et exploiter**  

- WorkoutDoors : **outil pivot**  
- Permet de transformer Apple en système ouvert  

### Référence formats

- **FIT** → format le plus complet  
- **TCX** → compromis interopérable  
- **GPX** → standard universel  

---

## Recommandation

Pour améliorer les exports Apple :

1. Utiliser WorkoutDoors comme couche d’export  
2. Conserver FIT comme format principal  
3. Générer TCX / GPX selon les usages  

➡️ Permet de construire un pipeline de données robuste et interopérable
