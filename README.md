# mapa-grzybiarza-data

Data for [mapa-grzybiarza](https://mapa-grzybiarza.matteuszd.workers.dev), written by GitHub Actions.

- Branch `main`: archive that only grows. Nothing here is ever rewritten or deleted.
  - `weather/YYYY/MM/DD.json.gz`: one final day of daily weather for every land cell of Poland. The header names the variables, the format version and the hash of `weather/cells.json`.
  - `weather/cells.json`: the list of grid cells the day files refer to.
  - `protected-areas/YYYY-MM-DD.geojson.gz`: national parks and nature reserves as fetched on that day.
- Branch `current`: one commit, replaced on every run. The working store and the files the app is built with.

## Sources and licences
- Weather: [Open-Meteo](https://open-meteo.com/), [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- Protected areas: Generalna Dyrekcja Ochrony Środowiska (GDOŚ), WFS `sdi.gdos.gov.pl`, simplified.
