# QUDT Units
Schema Doc:
http://www.qudt.org/qudt/owl/1.0.0/qudt/index.html

Unit Vocabulary:
http://qudt.org/1.1/vocab/OVG_units-qudt-(v1.1).ttl

Quantity:
http://qudt.org/1.1/schema/OSG_quantity-(v1.1).ttl


    @prefix qudt:    <http://qudt.org/schema/qudt#> .
    @prefix unit:    <http://qudt.org/vocab/unit#> .
    @prefix qudt-1.1:  <http://qudt.org/1.1/schema/qudt#> .
    @prefix qudt-unit-1.1:  <http://qudt.org/1.1/vocab/unit#> .


## Relevant Vocabularies

```
unit:Kilo
      rdf:type qudt:DecimalPrefixUnit ;
      rdfs:label "Kilo"^^xsd:string ;
      qudt:conversionMultiplier
              1.0E3 ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:symbol "k"^^xsd:string ;
      skos:exactMatch <http://dbpedia.org/resource/Kilo> .
unit:Milli
      rdf:type qudt:DecimalPrefixUnit ;
      rdfs:label "Milli"^^xsd:string ;
      qudt:conversionMultiplier
              1.0E-3 ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:symbol "m"^^xsd:string ;
      skos:exactMatch <http://dbpedia.org/resource/Milli-> .
unit:Giga
      rdf:type qudt:DecimalPrefixUnit ;
      rdfs:label "Giga"^^xsd:string ;
      qudt:conversionMultiplier
              1.0E9 ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:symbol "G"^^xsd:string ;
      skos:exactMatch <http://dbpedia.org/resource/Giga-> .

unit:Day
      rdf:type qudt:TimeUnit , qudt:UsedWithSIUnit ;
      rdfs:label "Day"^^xsd:string ;
      qudt:abbreviation "d"^^xsd:string ;
      qudt:code "0490"^^xsd:string ;
      qudt:conversionMultiplier
              "86400"^^xsd:double ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:description "Mean solar day"^^xsd:string ;
      qudt:symbol "d"^^xsd:string ;
      skos:exactMatch <http://dbpedia.org/resource/Day> .
unit:Year365Day
      rdf:type qudt:TimeUnit , qudt:NotUsedWithSIUnit ;
      rdfs:label "Year (365 Day)"^^xsd:string ;
      qudt:abbreviation "yr"^^xsd:string ;
      qudt:code "1980"^^xsd:string ;
      qudt:conversionMultiplier
              "31536000"^^xsd:double ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:symbol "yr"^^xsd:string .
unit:Byte
      rdf:type qudt:InformationEntropyUnit , qudt:DerivedUnit ;
      rdfs:label "Byte"^^xsd:string ;
      qudt:abbreviation "B"^^xsd:string ;
      qudt:code "3040"^^xsd:string ;
      qudt:conversionMultiplier
              "5.54517744"^^xsd:double ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:symbol "B"^^xsd:string ;
      skos:exactMatch <http://dbpedia.org/resource/Byte> .
```
Classes:
1. qudt:Unit
2. qudt:DataRateUnit
3. qudt:TimeUnit
4. qudt:DerivedUnit
5. qudt:VolumePerTimeUnit

Properties:   
1. qudt:quantityValue
2. qudt:numericValue
3. qudt:unit

## Hour
```
unit:Hour
      rdf:type qudt:UsedWithSIUnit , qudt:TimeUnit ;
      rdfs:label "Hour"^^xsd:string ;
      qudt:abbreviation "hr"^^xsd:string ;
      qudt:code "0830"^^xsd:string ;
      qudt:conversionMultiplier
              "3600.0"^^xsd:double ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:symbol "hr"^^xsd:string ;
      skos:exactMatch <http://dbpedia.org/resource/Hour> .
```

## MegabitsPerSecond
```
unit:MegabitsPerSecond
      rdf:type qudt:DerivedUnit , qudt:DataRateUnit ;
      rdfs:label "Megabit per Second"^^xsd:string ;
      qudt:abbreviation "mbps"^^xsd:string ;
      qudt:code "3015"^^xsd:string ;
      qudt:symbol "mbps"^^xsd:string .
```

## MilliSecond
```
unit:MilliSecond
      rdf:type qudt:DerivedUnit , qudt:TimeUnit ;
      rdfs:label "Millisecond"^^xsd:string ;
      qudt:abbreviation "ms"^^xsd:string ;
      qudt:code "1616"^^xsd:string ;
      qudt:conversionMultiplier
              "0.001"^^xsd:double ;
      qudt:conversionOffset
              "0.0"^^xsd:double ;
      qudt:symbol "ms"^^xsd:string ;
      skos:exactMatch <http://dbpedia.org/resource/Millisecond> .
```
# Release 2.0
Although there is QUDT second release, but we find that version 1.1 fits our needs better, also there are too many 2.0 Vocabularies are in progress like http://qudt.org/2.0/vocab/quantitykind/communications and http://qudt.org/2.0/schema/qudt/engineering, which could be what we meed.
