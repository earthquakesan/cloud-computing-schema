# Google Cloud: extract region codes from json imput useing jq
Related topics:
[Manually mapping Google Cloud regions](region.md)

# Version 1.41
## Getting Input
Data: original json for Google Cloud
https://cloudpricingcalculator.appspot.com/static/data/pricelist.json

[A cached version of the json input.](data/google/v1.41.json)

## Provider specific region codes
List of codes can be extracted from imput.
Apply transformation using `jq`, view the live snippet https://jqplay.org/s/IrbiQWTZbQ
```
def set(s): reduce s as $x ({}; .[$x | (type[0:1] + tostring)] = $x);

def distinct(s): set(s)[];

.gcp_price_list
| del(.sustained_use_base,.sustained_use_tiers)
| [ 
    distinct(.[]
           | keys_unsorted[] as $k
           | select( getpath([$k]) | type == "number")
           | $k)
] - ["maxNumberOfPd", "maxPdSize", "gceu"]
```
Result
```
[
  "us",
  "us-central1",
  "us-east1",
  "us-east4",
  "us-west1",
  "us-west2",
  "europe",
  "europe-west1",
  "europe-west2",
  "europe-west3",
  "europe-west4",
  "europe-north1",
  "northamerica-northeast1",
  "asia",
  "asia-east",
  "asia-northeast",
  "asia-southeast",
  "australia-southeast1",
  "australia",
  "southamerica-east1",
  "asia-south1",
  "asia-east1",
  "asia-northeast1",
  "asia-southeast1",
  "nam3",
  "nam-eur-asia1"
]
```

## SPARQL-Generate
[Construct Geonames mapping](region.md#GeoNames)
Run [queries](../sparql-generate/gcloud/region_inJurisdiction.rqg)
in [SPARQL-Generat Playground](https://ci.mines-stetienne.fr/sparql-generate/playground.html)
to get [results (RDF turtle)](../sparql-generate/result/gcloud/region_inJurisdiction.ttl)

# Version 1.62
New version of data updated on 12-February-2019.
While the ontology can still keep the same, the data collected needs to be updated.

https://cloud.google.com/compute/docs/regions-zones/
