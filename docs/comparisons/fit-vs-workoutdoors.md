# Comparaison FIT  
## Garmin vs WorkoutDoors (Apple)

Ce document compare les fichiers **FIT** générés par des appareils :contentReference[oaicite:0]{index=0} et par l’application :contentReference[oaicite:1]{index=1} sur Apple Watch.

L’objectif est d’identifier les différences de **structure**, de **champs**, et de **richesse des données**.

---

## Vue d’ensemble

| Critère | Garmin FIT | WorkoutDoors FIT |
|--------|------------|------------------|
| Format | FIT natif | FIT exporté |
| Conformité FIT SDK | ✔️ | ✔️ |
| Richesse des données | Très élevée | Élevée |
| Écosystème | Intégré | Dépend Apple Health |
| Interopérabilité | Élevée | Élevée |

---

## Structure des messages FIT

| Message | Garmin | WorkoutDoors |
|--------|--------|--------------|
| file_id | ✔️ | ✔️ |
| device_info | ✔️ | ✔️ |
| event | ✔️ | ✔️ |
| record | ✔️ | ✔️ |
| lap | ✔️ | ✔️ |
| session | ✔️ | ✔️ |
| activity | ✔️ | ✔️ |
| developer_fields | ✔️ | ✔️ |

---

## Données GPS (Record)

| Champ | Garmin | WorkoutDoors |
|------|--------|--------------|
| timestamp | ✔️ | ✔️ |
| position_lat / long | ✔️ | ✔️ |
| altitude | ✔️ | ✔️ |
| enhanced_altitude | ✔️ | ✔️ |
| speed | ✔️ | ✔️ |
| enhanced_speed | ✔️ | ✔️ |
| distance | ✔️ | ✔️ |
| gps_accuracy | ✔️ | ⚠️ |
| heading | ✔️ | ⚠️ |
| vertical_speed | ✔️ | ⚠️ |

---

## Données physiologiques

| Champ | Garmin | WorkoutDoors |
|------|--------|--------------|
| heart_rate | ✔️ | ✔️ |
| cadence | ✔️ | ✔️ |
| power | ✔️ | ✔️ (si capteur) |
| temperature | ✔️ | ✔️ |
| calories | ✔️ | ✔️ |

---

## Métriques avancées (différence majeure)

| Champ | Garmin | WorkoutDoors |
|------|--------|--------------|
| VO2max | ✔️ | ❌ |
| Training Effect | ✔️ | ❌ |
| Training Load | ✔️ | ❌ |
| Recovery Time | ✔️ | ❌ |
| Performance Condition | ✔️ | ❌ |

➡️ Ces métriques sont **propriétaires Garmin** et non présentes côté Apple.

---

## Running dynamics

| Champ | Garmin | WorkoutDoors |
|------|--------|--------------|
| vertical_oscillation | ✔️ | ⚠️ |
| ground_contact_time | ✔️ | ⚠️ |
| stride_length | ✔️ | ⚠️ |
| running_power | ✔️ | ⚠️ |

---

## Cyclisme avancé

| Champ | Garmin | WorkoutDoors |
|------|--------|--------------|
| power_balance | ✔️ | ✔️ |
| torque_effectiveness | ✔️ | ⚠️ |
| pedal_smoothness | ✔️ | ⚠️ |
| cycling_dynamics | ✔️ | ⚠️ |

---

## Laps et sessions

| Champ | Garmin | WorkoutDoors |
|------|--------|--------------|
| total_time | ✔️ | ✔️ |
| total_distance | ✔️ | ✔️ |
| avg_speed | ✔️ | ✔️ |
| max_speed | ✔️ | ✔️ |
| avg_heart_rate | ✔️ | ✔️ |
| max_heart_rate | ✔️ | ✔️ |
| avg_cadence | ✔️ | ✔️ |
| calories | ✔️ | ✔️ |
| ascent / descent | ✔️ | ✔️ |
| zones détaillées | ✔️ | ⚠️ |

---

## Capteurs et connectivité

| Élément | Garmin | WorkoutDoors |
|--------|--------|--------------|
| ANT+ | ✔️ | ❌ |
| Bluetooth capteurs | ✔️ | ✔️ |
| Multi-capteurs | ✔️ | ✔️ |
| Écosystème capteurs | Très riche | Limité |

---

## Navigation et parcours

| Champ | Garmin | WorkoutDoors |
|------|--------|--------------|
| course / route | ✔️ | ✔️ |
| course points | ✔️ | ✔️ |
| navigation instructions | ✔️ | ✔️ |
| cartographie | ✔️ | ✔️ (très avancée) |

---

## Qualité des données

| Critère | Garmin | WorkoutDoors |
|--------|--------|--------------|
| Fréquence GPS | 1 Hz / adaptatif | 1 Hz |
| Filtrage signal | Avancé | Standard |
| Précision globale | Très élevée | Élevée |

---

## Developer fields

| Élément | Garmin | WorkoutDoors |
|--------|--------|--------------|
| Champs custom | ✔️ | ✔️ |
| Compatibilité outils | ✔️ | ⚠️ |

---

## Différences clés

### Avantages Garmin
- Données physiologiques avancées
- Running / cycling dynamics complets
- Meilleur filtrage et précision
- Écosystème capteurs étendu (ANT+)

### Avantages WorkoutDoors
- Accès aux données Apple
- Export FIT complet depuis Apple
- Navigation et cartographie avancées
- Interopérabilité avec outils tiers

---

## Synthèse

| Critère | Meilleur |
|--------|---------|
| Richesse des données | Garmin |
| Compatibilité FIT | Égal |
| Navigation | WorkoutDoors |
| Écosystème capteurs | Garmin |
| Apple interopérable | WorkoutDoors |

---

## Conclusion

- **Garmin FIT** = référence industrielle (complet, structuré, enrichi)  
- **WorkoutDoors FIT** = export très solide mais dépendant des données Apple  

La différence principale réside dans :

- les **métriques avancées propriétaires Garmin**
- la **profondeur des données capteurs**

---

## Recommandation

- Analyse avancée → Garmin FIT  
- Usage Apple → WorkoutDoors FIT  
- Pipeline hybride → WorkoutDoors + conversion FIT  
