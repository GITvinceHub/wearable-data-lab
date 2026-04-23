# GPX

## Introduction

Le format **GPX** (**GPS Exchange Format**) est un standard ouvert basé sur XML, conçu pour échanger des données de géolocalisation.

Il est largement utilisé pour partager des **traces GPS**, des **routes** et des **waypoints**, indépendamment des plateformes ou des fabricants.

Contrairement à FIT ou TCX, GPX est centré sur la **géographie**, et non sur l’analyse sportive.

---

## Caractéristiques générales

| Critère | Description |
|--------|-------------|
| Type de format | XML |
| Lisibilité humaine | Oui |
| Taille de fichier | Élevée |
| Richesse des données | Limitée |
| Standard ouvert | Oui |
| Usage principal | GPS, cartographie, partage |

---

## Points forts

### Principaux avantages

- standard ouvert et universel  
- compatible avec la majorité des logiciels GPS  
- facile à lire et à modifier  
- idéal pour le partage de traces  
- support des routes et waypoints  

---

## Types de données généralement contenus

### Données de base

- latitude / longitude  
- altitude  
- horodatage  
- distance (calculée)  

### Données GPS spécifiques

- traces (`<trk>`)  
- routes (`<rte>`)  
- points d’intérêt (`<wpt>`)  

### Extensions possibles

- fréquence cardiaque  
- cadence  
- puissance  

⚠️ Ces extensions ne sont **pas standardisées** et dépendent des outils.

---

## Structure logique

Le format GPX est organisé en XML simple.

| Élément | Rôle |
|--------|------|
| `<gpx>` | racine |
| `<trk>` | trace |
| `<trkseg>` | segment |
| `<trkpt>` | point GPS |
| `<rte>` | route |
| `<wpt>` | waypoint |

---

## Niveau de richesse

| Donnée | GPX |
|--------|-----|
| GPS | ✔️ |
| Altitude | ✔️ |
| Timestamp | ✔️ |
| Fréquence cardiaque | ⚠️ |
| Cadence | ⚠️ |
| Puissance | ⚠️ |
| Température | ❌ |
| Laps / splits | ❌ |
| Sessions | ❌ |
| Événements | ❌ |
| Navigation | ✔️ |
| Capteurs externes | ❌ |

---

## Limites

- très peu adapté à l’analyse sportive  
- absence de structure avancée (laps, sessions)  
- perte importante d’informations lors de conversion depuis FIT  
- extensions non standardisées  
- fichiers volumineux  

---

## Cas d’usage recommandés

| Usage | Pertinence |
|------|-----------|
| Partage de traces GPS | Excellente |
| Cartographie | Excellente |
| Navigation | Excellente |
| Compatibilité universelle | Excellente |
| Analyse sportive | Faible |

---

## Comparaison rapide

| Format | Positionnement |
|--------|--------------|
| FIT | beaucoup plus complet |
| TCX | plus adapté au sport |
| Apple XML | beaucoup plus riche |

---

## Recommandations

Utiliser GPX pour :

- partager des parcours ou traces  
- visualiser des activités sur une carte  
- assurer une compatibilité maximale  

Éviter GPX pour :

- l’analyse de performance  
- la conservation des données complètes  

---

## Conclusion

Le format GPX est le standard universel pour les données GPS. Il est simple, lisible et interopérable, mais reste limité pour les usages sportifs avancés.

Il est recommandé comme format d’échange, mais pas comme format principal de stockage.
