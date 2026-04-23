# TCX

## Introduction

Le format **TCX** (**Training Center XML**) est un format XML utilisé pour stocker et échanger des activités sportives. Il a été introduit pour structurer les données d’entraînement de manière lisible et interopérable.

Contrairement au format FIT, TCX privilégie la **lisibilité** et la **compatibilité**, au détriment d’une partie de la richesse des données.

---

## Caractéristiques générales

| Critère | Description |
|--------|-------------|
| Type de format | XML |
| Lisibilité humaine | Oui |
| Taille de fichier | Moyenne |
| Richesse des données | Élevée |
| Standard ouvert | Non (mais largement adopté) |
| Usage principal | Échange de données sportives |

---

## Points forts

### Principaux avantages

- format lisible et structuré  
- facile à parser (XML standard)  
- bonne compatibilité avec les logiciels sportifs  
- support des laps et des sessions  
- adapté aux échanges entre plateformes  

---

## Types de données généralement contenus

### Données de base

- horodatage  
- latitude / longitude  
- altitude  
- distance  
- vitesse  

### Données physiologiques

- fréquence cardiaque  
- cadence  
- calories  

### Données partiellement supportées

- puissance (selon implémentation)  
- extensions personnalisées  

---

## Structure logique

Le format TCX est organisé en XML hiérarchique.

| Élément | Rôle |
|--------|------|
| `<TrainingCenterDatabase>` | racine |
| `<Activities>` | liste des activités |
| `<Activity>` | activité individuelle |
| `<Lap>` | segment / tour |
| `<Track>` | série de points |
| `<Trackpoint>` | point de mesure |

---

## Niveau de richesse

| Donnée | TCX |
|--------|-----|
| GPS | ✔️ |
| Altitude | ✔️ |
| Fréquence cardiaque | ✔️ |
| Cadence | ✔️ |
| Puissance | ⚠️ |
| Température | ❌ |
| Laps / splits | ✔️ |
| Sessions | ✔️ |
| Événements | ✔️ |
| Running dynamics | ❌ |
| Capteurs externes | ❌ |

---

## Limites

- moins riche que FIT  
- certaines données dépendantes d’extensions  
- absence de nombreuses métriques avancées  
- taille de fichier plus importante que FIT  

---

## Cas d’usage recommandés

| Usage | Pertinence |
|------|-----------|
| Échange entre plateformes | Excellente |
| Analyse standard | Bonne |
| Archivage complet | Moyenne |
| Compatibilité logicielle | Excellente |
| Données avancées | Limitée |

---

## Comparaison rapide

| Format | Positionnement |
|--------|--------------|
| FIT | plus complet mais moins lisible |
| GPX | plus universel mais moins riche |
| Apple XML | plus riche mais plus complexe |

---

## Recommandations

Utiliser TCX pour :

- transférer des activités entre applications  
- assurer la compatibilité avec des outils sportifs  
- conserver une structure claire et exploitable  

Éviter TCX pour :

- l’analyse avancée  
- la conservation de données complètes  

---

## Conclusion

Le format TCX constitue un bon compromis entre **richesse des données** et **facilité d’exploitation**. Il reste très utilisé pour l’échange d’activités, bien qu’il soit progressivement supplanté par FIT pour les usages avancés.
