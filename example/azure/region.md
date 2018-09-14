# Data Mapping: Microsoft Azure Cloud Regions
## Getting Input
Data: original json for Azure Cloud
https://azure.microsoft.com/api/v2/pricing/virtual-machines-base/calculator/?culture=en-au&discount=mosp
[A cached version of the json input.](../data/azure/vm_base.json)
## human-readbale name to slug mapping
Obtained by run
```
.regions | 
[
  to_entries[] |
  {
    "key": .value.displayName, 
    "value": .value.slug
  }
] | from_entries
```
on [input](#Getting-Input)

Try live on jq playground https://jqplay.org/s/eRBisoYbDb

Result: [region.json](../jq/azure/region.json)

## Geonames Mapping
See example in [geonames_rdf](../geonames_rdf/azure/) directory.

## SPARQL-Generate
Run [queries](../sparql-generate/azure/region.rqg)
in [SPARQL-Generat Playground](https://ci.mines-stetienne.fr/sparql-generate/playground.html)
to get [results (RDF turtle)](../sparql-generate/result/azure/region.ttl)
