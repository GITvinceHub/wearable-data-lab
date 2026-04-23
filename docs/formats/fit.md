# FIT

## Introduction

Le format **FIT** (**Flexible and Interoperable Data Transfer**) est un format binaire utilisé principalement pour enregistrer des activités sportives, des données de capteurs et des métriques de performance.

Il est particulièrement associé à l’écosystème Garmin, mais il est également pris en charge par de nombreux logiciels d’analyse sportive et certaines applications tierces. Son principal intérêt est de permettre un stockage **compact**, **structuré** et **riche en données**, bien au-delà d’une simple trace GPS.

---

## Caractéristiques générales

| Critère | Description |
|--------|-------------|
| Type de format | Binaire |
| Lisibilité humaine | Non |
| Taille de fichier | Faible |
| Richesse des données | Très élevée |
| Standard ouvert | Non |
| Usage principal | Activités sportives, capteurs, performance |

---

## Points forts

### Principaux avantages

- stockage compact  
- prise en charge des métriques avancées  
- structure hiérarchique claire  
- gestion des laps, sessions et événements  
- support de nombreux capteurs  
- bonne compatibilité avec les outils d’analyse sportive  

---

## Types de données généralement contenus

### Données de base

- horodatage  
- latitude / longitude  
- altitude  
- distance  
- vitesse  
- durée  

### Données physiologiques

- fréquence cardiaque  
- cadence  
- puissance  
- calories  
- température  

### Données avancées possibles

- VO2max  
- training effect  
- training load  
- recovery time  
- performance condition  
- running dynamics  
- cycling dynamics  
- équilibre gauche / droite  
- navigation  

---

## Structure logique

Un fichier FIT est organisé autour de messages normalisés.

| Message | Rôle |
|--------|------|
| `file_id` | identification du fichier |
| `device_info` | informations appareil |
| `event` | début, pause, reprise, fin |
| `record` | points de mesure successifs |
| `lap` | tours / segments |
| `session` | résumé global |
| `activity` | clôture |
| `developer_fields` | champs personnalisés |

---

## Niveau de richesse

| Donnée | FIT |
|--------|-----|
| GPS | ✔️ |
| Altitude | ✔️ |
| Fréquence cardiaque | ✔️ |
| Cadence | ✔️ |
| Puissance | ✔️ |
| Température | ✔️ |
| Laps / splits | ✔️ |
| Sessions | ✔️ |
| Événements | ✔️ |
| Running dynamics | ✔️ |
| Capteurs externes | ✔️ |

---

## Limites

- non lisible directement  
- dépendance à des outils spécialisés  
- format non ouvert  
- présence de champs propriétaires  

---

## Cas d’usage recommandés

| Usage | Pertinence |
|------|-----------|
| Archivage complet | Excellente |
| Analyse performance | Excellente |
| Comparaison technique | Excellente |
| Partage simple | Moyenne |
| Interop universelle | Limitée |

---

## Comparaison rapide

| Format | Positionnement |
|--------|--------------|
| TCX | plus simple mais moins riche |
| GPX | universel mais très limité |
| Apple XML | riche mais difficile à exploiter |

---

## Recommandations

Utiliser FIT comme format principal pour :

- conserver les données complètes  
- analyse avancée  
- éviter les pertes lors des conversions  

Puis exporter en :

- TCX → compatibilité  
- GPX → cartographie  

---

## Conclusion

Le format FIT est la référence pour les données d’activité sportives avancées. Il offre le meilleur compromis entre compacité et richesse, au prix d’une complexité technique plus élevée.
