# jsonmaps-finland
Contains maps of Finland in GeoJSON and TopoJSON formats. GeoJSON maps are RFC 7946 compliant so they use counter-clockwise winding order. TopoJSON uses the opposite winding order.

## GeoJSON to TopoJSON conversion
GeoJSON maps are converted to TopoJSON using mapshaper. Mapshaper changes the winding order correctly unlike topojson-server.

## Using with d3
When using maps with D3 note that D3 uses opposite winding order to RFC 7946. Winding order should be reversed when using GeoJSON maps in this package with d3-geo. However, when using TopoJSON maps in this package with topojson-client and d3-geo the winding order is correct. This is because topojson-client  (nor topojson-server) does not seem to change the winding order.

## Map source and licence
 [Statistics Finland](https://www.stat.fi/org/avoindata/paikkatietoaineistot_en.html). CC BY 4.0.