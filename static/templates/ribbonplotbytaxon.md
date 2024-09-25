```template
id: ribbonPlotByTaxon
title: Ribbon plot using BUSCO genes by taxon
description: |
  Show locations of all BUSCO genes shared between a pair of species
valueA_example: Cepaea hortensis
valueA_label: Taxon A
valueA_description: |
  Taxon name or ID to plot on x-axis
valueB_example: Achatina immaculata
valueB_label: Taxon B
valueB_description: |
  Taxon name or ID to plot on y-axis
valueC_example: mollusca_odb10
valueC_label: BUSCO lineage
valueC_description: |
  Odb10 BUSCO lineage to use for comparison
url:
  path: /search
  query: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type={valueC}-busco-gene AND busco_status!=duplicated
  queryA: assembly--tax_name({valueA}) AND refseq_category=representative genome,reference genome
  queryB: assembly--tax_name({valueB}) AND refseq_category=representative genome,reference genome
  xOpts: ";;;;{valueA}"
  yOpts: ";;;;{valueB}"
  result: feature
  taxonomy: ncbi
  report: ribbon
reorient: true
compactLegend: true
```
