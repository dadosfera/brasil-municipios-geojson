# GeoJSON do Brasil: municípios e estados

Este geojson foi criado com o objetivo de gerar uma visualização do mapa do Brasil no Metabase.

O repositório também inclui os limites estaduais do projeto
[geodata-br-states](https://github.com/giuliano-macedo/geodata-br-states).
Os dados municipais originais foram preservados.

## Arquivos disponíveis

| Dados | Arquivo | Propriedades para identificação |
| --- | --- | --- |
| Municípios do Brasil | [geojs-100-mun-v2.json](geojs-100-mun-v2.json) | `id`, `name`, `uf_municipio` |
| 27 unidades federativas | [geojson/br_states.json](geojson/br_states.json) | `SIGLA`, `Estado` |
| Uma unidade federativa | [geojson/br_states/](geojson/br_states/) (`br_<uf>.json`, sigla em minúsculas) | `SIGLA`, `Estado` |

Por exemplo: [Alagoas](geojson/br_states/br_al.json),
[São Paulo](geojson/br_states/br_sp.json) e
[Distrito Federal](geojson/br_states/br_df.json).

No Metabase, use a propriedade correspondente à chave dos seus dados:
`id` ou `uf_municipio` para municípios e `SIGLA` ou `Estado` para estados.
Os arquivos estaduais mantêm as propriedades originais da fonte; atributos
demográficos não devem ser interpretados como dados atuais.

## Origem e licenças

Os arquivos estaduais foram importados do projeto
[geodata-br-states](https://github.com/giuliano-macedo/geodata-br-states),
que indica LAGEAMB / UFPR como fonte dos limites estaduais.
Commit de origem: `32d7169859c5dad3bd7ae4f2710733b96b02d40f`.
Copyright (c) 2023 Giuliano Oliveira de Macedo.

A [licença original deste repositório](LICENSE) foi preservada.
Os arquivos importados continuam sob a
[licença MIT do projeto de origem](LICENSES/geodata-br-states-MIT.txt).

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
