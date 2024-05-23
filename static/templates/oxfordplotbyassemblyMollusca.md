```template
id: oxfordPlotByAssemblyMollusca
title: Oxford plot using BUSCO genes by assembly showing ancestral linkage groups
description: |
  Show locations of all BUSCO genes shared between a pair of assemblies with ancestral linkage groups
valueA_example: GCA_963676685.2
valueA_label: Assembly accession A
valueA_description: |
  Assembly GCA accession to plot on x-axis
valueB_example: GCA_017311375.1
valueB_label: Assembly accession B
valueB_description: |
  Assembly GCA accession to plot on y-axis
valueC_example: mollusca_odb10
valueC_label: BUSCO lineage
valueC_description: |
  Odb10 BUSCO lineage to use for comparison
url:
  path: /search
  query: assembly_id={valueA},{valueB} AND collate(sequence_id,busco_gene) AND feature_type={valueC}-busco-gene AND busco_status!=duplicated AND ancestral_unit
  cat: "ancestral_unit[20]=Moll1,Moll2,Moll3,Moll4,Moll5,Moll6,Moll7,Moll8,Moll9,Moll10,Moll11,Moll12,Moll13,Moll14,Moll15,Moll16,Moll17,Moll18,Moll19,Moll20"
  result: feature
  taxonomy: ncbi
  report: oxford
```
