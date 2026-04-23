# Comparaison des formats d’activités sportives  
## FIT vs TCX vs GPX vs Apple Health XML

Ce document fournit une comparaison technique structurée des principaux formats utilisés pour stocker et échanger des activités sportives issues de montres GPS et smartphones.

---

## Introduction

Les activités sportives (course, vélo, randonnée, etc.) sont enregistrées sous différents formats selon les écosystèmes :

- **FIT** : format binaire propriétaire optimisé pour la performance et la richesse des données, utilisé notamment par Garmin  
- **TCX** : format XML structuré orienté sport, historiquement utilisé pour l’échange de données  
- **GPX** : standard ouvert centré sur la géolocalisation  
- **Apple XML** : export global des données de santé via Apple Health  

Chaque format implique des compromis entre :

- richesse des données  
- interopérabilité  
- facilité d’analyse  
- taille des fichiers  

---

## Tableau comparatif global

| Critère | FIT | TCX | GPX | Apple Health XML |
|--------|-----|-----|-----|------------------|
| Type | Binaire | XML | XML | XML |
| Origine | Garmin | Garmin | Standard ouvert | Apple |
| Lisibilité humaine | ❌ | ✔️ | ✔️ | ✔️ |
| Taille fichier | Très faible | Moyenne | Élevée | Très élevée |
| Standard ouvert | ❌ | ❌ | ✔️ | ❌ |
| Interopérabilité | Moyenne | Bonne | Excellente | Faible |

---

## Données contenues

| Donnée | FIT | TCX | GPX | Apple XML |
|--------|-----|-----|-----|-----------|
| Latitude / Longitude | ✔️ | ✔️ | ✔️ | ✔️ |
| Altitude | ✔️ | ✔️ | ✔️ | ✔️ |
| Timestamp | ✔️ | ✔️ | ✔️ | ✔️ |
| Fréquence cardiaque | ✔️ | ✔️ | ⚠️ | ✔️ |
| Cadence | ✔️ | ✔️ | ⚠️ | ✔️ |
| Puissance | ✔️ | ⚠️ | ⚠️ | ✔️ |
| Température | ✔️ | ❌ | ❌ | ✔️ |
| Calories | ✔️ | ✔️ | ❌ | ✔️ |
| VO2max | ✔️ | ❌ | ❌ | ✔️ |
| Running dynamics | ✔️ | ❌ | ❌ | ⚠️ |
| Capteurs externes | ✔️ | ❌ | ❌ | ✔️ |

---

## Structure des activités

| Élément | FIT | TCX | GPX | Apple XML |
|--------|-----|-----|-----|-----------|
| Points (trackpoints) | ✔️ | ✔️ | ✔️ | ✔️ |
| Laps / splits | ✔️ | ✔️ | ❌ | ✔️ |
| Sessions | ✔️ | ✔️ | ❌ | ✔️ |
| Multi-sport | ✔️ | ⚠️ | ❌ | ✔️ |
| Événements (pause, reprise) | ✔️ | ✔️ | ❌ | ✔️ |
| Navigation / parcours | ✔️ | ❌ | ✔️ | ❌ |

---

## Facilité d’exploitation

| Critère | FIT | TCX | GPX | Apple XML |
|--------|-----|-----|-----|-----------|
| Analyse avancée | ✔️✔️✔️ | ✔️✔️ | ✔️ | ❌ |
| Parsing technique | Complexe | Facile | Très facile | Complexe |
| Compatibilité outils | Élevée | Très élevée | Universelle | Faible |
| Conversion facile | ⚠️ | ✔️ | ✔️ | ❌ |

---

## Pertes de données lors conversion

| Conversion | Perte estimée | Détails |
|-----------|--------------|--------|
| FIT → TCX | 20–40% | perte des métriques avancées |
| FIT → GPX | 60–80% | perte capteurs + structure |
| TCX → GPX | 30–50% | perte laps et données sportives |
| Apple XML → GPX | Très élevée | reconstruction nécessaire |
| GPX → FIT | ❌ | impossible de recréer les données |

---

## Cas d’usage recommandés

| Usage | Format recommandé |
|------|------------------|
| Archivage complet | FIT |
| Analyse performance | FIT |
| Compatibilité logiciels | TCX |
| Partage GPS | GPX |
| Export Apple exploitable | FIT (via app tierce) |

---

## Lecture synthétique

- **FIT** → format le plus complet, adapté à l’analyse avancée  
- **TCX** → bon compromis entre richesse et compatibilité  
- **GPX** → standard universel, limité aux données GPS  
- **Apple XML** → très riche mais peu exploitable directement  

---

## Conclusion

Le choix du format dépend du besoin :

- Analyse avancée → **FIT**  
- Interopérabilité → **TCX / GPX**  
- Cartographie simple → **GPX**  
- Écosystème Apple → nécessite conversion  

Dans une architecture robuste, il est recommandé de :

- conserver les fichiers **FIT comme source primaire**  
- générer des exports **TCX / GPX selon les usages**  
