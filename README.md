 @@ -1,37 +1,43 @@
![tileserver-gl](https://cloud.githubusercontent.com/assets/59284/18173467/fa3aa2ca-7069-11e6-86b1-0f1266befeb6.jpeg)


# TileServer GL
[![Build Status](https://travis-ci.org/maptiler/tileserver-gl.svg?branch=master)](https://travis-ci.org/maptiler/tileserver-gl)
[![Docker Hub](https://img.shields.io/badge/docker-hub-blue.svg)](https://hub.docker.com/r/maptiler/tileserver-gl/)

Vector and raster maps with GL styles. Server side rendering by Mapbox GL Native. Map tile server for Mapbox GL JS, Android, iOS, Leaflet, OpenLayers, GIS via WMTS, etc.

## Using Docker

An alternative to npm to start the packed software easier is to install [Docker](https://www.docker.com/) on your computer and then run in the directory with the downloaded MBTiles the command:

```bash
docker build -t blockincrement/tileserver-gl .
```
```bash
docker run --rm -it -v $(pwd):/data -p 8080:80 blockincrement/tileserver-gl
```

This will download and start a ready to use container on your computer and the maps are going to be available in webbrowser on localhost:8080.

On laptop you can use [Docker Kitematic](https://kitematic.com/) and search "tileserver-gl" and run it, then drop in the 'data' folder the MBTiles.

## Adding tiles

Extra features added by our fork are a new folder called tiles that accepts .mbtile files and auto imports them into the server. 
Extra features added by our fork are a new folder called tiles that accepts .mbtile files and auto imports them into the server. Maptiles can be downloaded from [OpenMapTiles](https://openmaptiles.org/).

Make sure that the docker file name is correct before running.

```bash
docker run --rm -p 8080:80 blockincrement/tileserver-gl
```

## Line endings
Incase you get an error message when running the docker file that looks like this:
```bash
/usr/src/app/run.sh: line 1: syntax error near unexpected token `$'{\r''
'usr/src/app/run.sh: line 1: `_term() {
```
Open the run. sh file and change the CRLF to LF (This can be found in the lower right corner in VSCode).
## Documentation

You can read full documentation of this project at https://tileserver.readthedocs.io/.
