# leaflet-cc [![NPM version](https://badge.fury.io/js/leaflet-cc.svg)](https://npmjs.org/package/leaflet-cc) [![Build Status](https://travis-ci.org/bitbucket%20/leaflet-cc.svg?branch=master)](https://travis-ci.org/bitbucket%20/leaflet-cc)

> leaflet-cc
Arma Map into web sat map

## How to install?
osgeo4w-setup-x86_64.exe in ./installer ausführen und GDAL installieren (der rest ist optional)
 
## How to work with the tools? 
1. mit den Cheat Command die Map exportieren: https://community.bistudio.com/wiki/ArmA:_Cheats#TOPOGRAPHY
2. die emf auf das EmfToPNG tools ziehen
3. dann die OSGeoShell4W öffnen
4. dann in den ordner in dem sich die png befindet navigieren
5. gdal_translate -of PNG -outsize 16384 16384 quell_png_name rez_png_name //(als erstes müssen wir das Bild rezisen)
6. gdal2tiles -p raster -z 0-6 -w none rez_png_name sat //(packt alles in die getrennten tiles)
7. gdal_translate -of PNG -outsize 16384 16384 quell_png_name_non_grid rez_png_name //(als erstes müssen wir das Bild rezisen)
8. gdal2tiles -p raster -z 0-6 -w none rez_png_name_nongrid nongridsat //(packt alles in die getrennten tiles)







