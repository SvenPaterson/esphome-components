A fix for the m5stack atom echo compilation via esphome dashboard running on windows
Windows does not play well with magic lib so this code is modified to use the puremagic lib instead to fetch the wavefile

replace the ref to jesserockz github project in the m5stack-atom-echo.yaml:

external_components:
  - source: github://pr#5230
    components:
      - esp_adf
    refresh: 0s
  - source: github://jesserockz/esphome-components
    components: [file]
    refresh: 0s

    to

external_components:
  - source: github://pr#5230
    components:
      - esp_adf
    refresh: 0s
  - source: github://SvenPaterson/esphome-components
    components: [file]
    refresh: 0s
