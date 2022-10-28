# Geojson do Brasil dividido por municípios

Este geojson foi criado com o objetivo de gerar uma visualização do mapa do Brasil no Metabase.

## Estrutura de cada município no arquivo:

`{"type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "id": "1100015",
        "name": "Alta Floresta D'Oeste",
        "description": "Alta Floresta D'Oeste",
        "uf_municipio": "RO - Alta Floresta D'oeste"
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [...]
        }
    }
    ...]
}`