# Fibaro Custom V2

Intégration Fibaro personnalisée pour Home Assistant, basée sur l'intégration
officielle (version core **2026.9.0**) avec les ajouts suivants :

## Personnalisations par rapport à l'officiel

- **Media player** : support des TV pilotées via uiCallbacks du HC3
  (SamsungTV, X96Mini), mapping `deviceRole=TvSet` → media_player
- **Climate** : support de `com.fibaro.hvacSystemHeat` avec les modes
  français du HC3 (Off / Eco / Hors-Gel / Confort)
- **Cover** : lamelles (tilt) uniquement pour `deviceRole=VenetianBlinds`
  (corrige le faux tilt du FGR224 qui expose toujours value2)
- **Sensor** : capteur d'eau `com.fibaro.waterMeter` (litres, total croissant)
- **Typemap étendu** : ~30 types d'appareils supplémentaires reconnus
- **Zones suggérées** : les appareils héritent de la pièce définie dans le HC
- **pyfibaro 0.8.3 vendorisé** avec 2 patchs :
  - déduction du contrôleur caché (comptes sans droits admin)
  - `execute_callAction` / `uiCallbacks` pour le media player

## Installation

Via HACS (dépôt personnalisé) ou copie manuelle du dossier
`custom_components/fibaro_custom_v2` dans `config/custom_components/`.

**Requiert Home Assistant 2026.9.0 ou plus récent.**

## Version

2.1.0 — resynchronisé avec le code officiel HA core 2026.9.0
