---
title: CityGML Feature JSON Schema (Schema)

language_tabs:
  - json: JSON
  - jsonld: JSON-LD
  - turtle: RDF/Turtle

toc_footers:
  - Version 1.0
  - <a href='#'>CityGML Feature JSON Schema</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: CityGML Feature JSON Schema (Schema)
---


# CityGML Feature JSON Schema `ogc.geo.citygml.CityFeatureJSON`

A Generic OGC API Features compliant JSON schema. The schema is derived from the CityGML UML model

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong><a href="https://github.com/ogcincubator/CityGMLProfiles/blob/master/build/tests/geo/citygml/CityFeatureJSON/" target="_blank">valid</a></strong>
</aside>

# Description

## CityGML as JSON based on FG-JSON schema





# Examples

## GeoJSON - specialisation example.



```json
{
  "@context": {
    "mynamespace": "http://example.org/ns1/"
  },
  "id": "f1",
  "type": "Feature",
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [
        -111.67183507997295,
        40.056709946862874
      ],
      [
        -111.71,
        40.156709946862874
      ]
    ]
  },
  "properties": {
    "a": "mynamespace:aThing",
    "b": 23,
    "c": 0.1
  }
}

```

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/tests/geo/citygml/CityFeatureJSON/example_1_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2FCityGMLProfiles%2Fmaster%2Fbuild%2Ftests%2Fgeo%2Fcitygml%2FCityFeatureJSON%2Fexample_1_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




```jsonld
{
  "@context": [
    "https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/annotated/geo/citygml/CityFeatureJSON/context.jsonld",
    {
      "mynamespace": "http://example.org/ns1/"
    }
  ],
  "id": "f1",
  "type": "Feature",
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [
        -111.67183507997295,
        40.056709946862874
      ],
      [
        -111.71,
        40.156709946862875
      ]
    ]
  },
  "properties": {
    "a": "mynamespace:aThing",
    "b": 23,
    "c": 0.1
  }
}
```

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/tests/geo/citygml/CityFeatureJSON/example_1_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2FCityGMLProfiles%2Fmaster%2Fbuild%2Ftests%2Fgeo%2Fcitygml%2FCityFeatureJSON%2Fexample_1_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://example.com/features/f1> a geojson:Feature ;
    geojson:geometry [ a geojson:LineString ;
            geojson:coordinates ( ( -1.116718e+02 4.005671e+01 ) ( -1.1171e+02 4.015671e+01 ) ) ] .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/tests/geo/citygml/CityFeatureJSON/example_1_1.ttl">Open in new window</a>
</blockquote>



# JSON Schema

```yaml--schema
$schema: https://json-schema.org/draft/2020-12/schema
description: Example of a sinmple GeoJSON Feature specialisation
$ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/features/feature/schema.yaml

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2FCityGMLProfiles%2Fmaster%2Fbuild%2Fannotated%2Fgeo%2Fcitygml%2FCityFeatureJSON%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/annotated/geo/citygml/CityFeatureJSON/schema.yaml" target="_blank">https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/annotated/geo/citygml/CityFeatureJSON/schema.yaml</a>
* JSON version: <a href="https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/annotated/geo/citygml/CityFeatureJSON/schema.json" target="_blank">https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/annotated/geo/citygml/CityFeatureJSON/schema.json</a>


# JSON-LD Context

```json--ldContext
{
  "@context": {
    "type": "@type",
    "id": "@id",
    "properties": "@nest",
    "geometry": {
      "@context": {
        "coordinates": {
          "@container": "@list",
          "@id": "geojson:coordinates"
        }
      },
      "@id": "geojson:geometry"
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "links": {
      "@context": {
        "href": {
          "@type": "@id",
          "@id": "oa:hasTarget"
        },
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "type": "dct:type",
        "hreflang": "dct:language",
        "title": "rdfs:label",
        "length": "dct:extent"
      },
      "@id": "rdfs:seeAlso"
    },
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "@version": 1.1
  }
}
```

> <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2FCityGMLProfiles%2Fmaster%2Fbuild%2Fannotated%2Fgeo%2Fcitygml%2FCityFeatureJSON%2Fcontext.jsonld">View on JSON-LD Playground</a>

You can find the full JSON-LD context here:
<a href="https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/annotated/geo/citygml/CityFeatureJSON/context.jsonld" target="_blank">https://raw.githubusercontent.com/ogcincubator/CityGMLProfiles/master/build/annotated/geo/citygml/CityFeatureJSON/context.jsonld</a>

# References

* [OGC API - Features, Part 1, 7.16.2: Feature Response](https://docs.ogc.org/is/17-069r3/17-069r3.html#_response_7)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/CityGMLProfiles" target="_blank">https://github.com/ogcincubator/CityGMLProfiles</a>
* Path:
<code><a href="https://github.com/ogcincubator/CityGMLProfiles/blob/HEAD/_sources/CityFeatureJSON" target="_blank">_sources/CityFeatureJSON</a></code>

