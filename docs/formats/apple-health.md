# Apple Health XML

## Introduction

Le format **Apple Health XML** est le format d’export des données de santé issues de :contentReference[oaicite:0]{index=0}.

Il regroupe l’ensemble des données collectées par les appareils Apple (iPhone, Apple Watch), incluant les activités sportives, les mesures physiologiques et les métadonnées associées.

Contrairement aux formats FIT, TCX ou GPX, il ne s’agit pas d’un format dédié uniquement aux activités, mais d’un **export global du système de santé Apple**.

---

## Caractéristiques générales

| Critère | Description |
|--------|-------------|
| Type de format | XML |
| Lisibilité humaine | Oui |
| Taille de fichier | Très élevée |
| Richesse des données | Très élevée |
| Standard ouvert | Non |
| Usage principal | Export global des données de santé |

---

## Points forts

### Principaux avantages

- contient toutes les données disponibles dans Apple Health  
- grande richesse de métriques (santé + sport)  
- historisation complète  
- cohérence avec l’écosystème Apple  
- extensible via métadonnées  

---

## Types de données généralement contenus

### Données d’activité

- type d’activité (course, marche, vélo, etc.)  
- durée  
- distance  
- calories  
- énergie active  

### Données physiologiques

- fréquence cardiaque  
- variabilité de fréquence cardiaque (HRV)  
- VO2max (estimé)  
- saturation O₂ (SpO2)  
- température  
- sommeil  

### Données GPS

- positions (indirectes, via workouts)  
- routes (non toujours directement exploitables)  

### Données supplémentaires

- métadonnées détaillées  
- sources de données (appareil, app)  
- timestamps précis  
- données multi-applications  

---

## Structure logique

Le fichier XML exporté (`export.xml`) contient plusieurs types d’éléments.

| Élément | Rôle |
|--------|------|
| `<HealthData>` | racine |
| `<Record>` | données individuelles (mesures) |
| `<Workout>` | activité sportive |
| `<ActivitySummary>` | résumé d’activité |
| `<MetadataEntry>` | métadonnées |

---

## Niveau de richesse

| Donnée | Apple Health XML |
|--------|-----------------|
| GPS | ✔️ (indirect) |
| Altitude | ✔️ |
| Fréquence cardiaque | ✔️ |
| Cadence | ✔️ |
| Puissance | ✔️ (selon app) |
| Température | ✔️ |
| Calories | ✔️ |
| VO2max | ✔️ |
| Running dynamics | ⚠️ |
| Capteurs externes | ✔️ |
| Données santé avancées | ✔️✔️✔️ |

---

## Limites

- format très volumineux  
- difficile à exploiter directement  
- non structuré spécifiquement pour le sport  
- absence de standardisation pour l’export d’activités  
- nécessite des outils pour extraction et transformation  

---

## Cas d’usage recommandés

| Usage | Pertinence |
|------|-----------|
| Archivage complet des données Apple | Excellente |
| Analyse santé globale | Excellente |
| Analyse sportive directe | Faible |
| Interopérabilité | Faible |
| Conversion vers formats sportifs | Nécessaire |

---

## Comparaison rapide

| Format | Positionnement |
|--------|--------------|
| FIT | mieux structuré pour le sport |
| TCX | plus simple pour activités |
| GPX | plus adapté à la cartographie |
| Apple XML | plus riche mais moins exploitable |

---

## Recommandations

Utiliser Apple Health XML pour :

- exporter l’ensemble des données Apple  
- analyser des tendances long terme  
- conserver un historique complet  

Transformer ensuite vers :

- FIT → analyse sportive avancée  
- TCX → compatibilité  
- GPX → cartographie  

---

## Conclusion

Le format Apple Health XML est extrêmement riche mais peu adapté à une utilisation directe. Il constitue une **source de données brute**, nécessitant transformation pour être pleinement exploitable dans des workflows sportifs ou analytiques.

Il est essentiel dans une logique d’extraction de données, mais rarement utilisé tel quel.
