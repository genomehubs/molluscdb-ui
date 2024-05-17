```template
id: windowPlotByTaxon
title: Window statistic plot by taxon
description: |
  Show values of a statistic for windows along each chromosome in the primary assembly for a taxon
valueA_example: Quercus robur
valueA_label: Taxon name
valueA_description: |
  Taxon name or ID to plot statistics for
valueB_example: gc
valueB_label: Statistic
valueB_description: |
  Window-based statistic to plot along chromosomes. Options include: gc, masked, busco_count
valueC_example: 0.01
valueC_label: window-size
valueC_description: |
  Window size. Options include: 1000000, 100000, 0.1 & 0.01
url:
  path: /search
  queryA: assembly--tax_name({valueA}) AND refseq_category=representative genome,reference genome
  query: midpoint_proportion AND assembly_id=queryA.assembly_id AND feature_type=window-{valueC} AND {valueB}
  report: scatter
  y: "{valueB}"
  cat: sequence_id[50]
  includeEstimates: true
  scatterThreshold: -1
  result: feature
  taxonomy: ncbi
```
