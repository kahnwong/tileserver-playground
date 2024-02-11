# tileserver-playground

<https://github.com/maptiler/tileserver-gl>


## Download sample data

### Styles

Need to modify `styles.json` as outlined [here](https://www.blef.fr/how-to-deploy-tile-server/)

- <https://openmaptiles.org/styles/>
- <https://data.maptiler.com/maps/>
- <https://github.com/maptiler/tileserver-gl/releases/download/v1.3.0/test_data.zip>

### Mbtiles

- <https://data.maptiler.com/downloads/planet/>

#### Create mbtiles from OSM dump

Download `*.osm.pbf` file from <https://download.geofabrik.de/>, then use <https://github.com/systemed/tilemaker> to convert it to mbtiles:

```bash
tilemaker --input data/thailand-latest.osm.pbf --output data/thailand.mbtiles --process resources/process-openmaptiles.lua --config resources/config-openmaptiles.json
```

## Launch tileserver

```bash
docker compose up
```
