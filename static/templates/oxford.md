::breadcrumbs[Oxford plots]

Oxford plots allow you to visualize synteny and rearrangements between pairs of genomes. Patterns in linkage group and gene order conservation differ across lineages.

As the distance between species increases for these bivalves, fewer shared genes remain in the same order and orientation, though remnants of ancestral linkage groups persist. Such plots help uncover genomic architecture evolution.

:::grid{container direction="row" spacing="1" inline}

```report
report: oxford
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type=metazoa_odb10-busco-gene AND busco_status!=duplicated AND ancestral_unit
queryA: assembly--tax_name(Mytilus edulis)
queryB: assembly--tax_name(Mytilus coruscus)
cat: "ancestral_unit[20]=Moll1,Moll2,Moll3,Moll4,Moll5,Moll6,Moll7,Moll8,Moll9,Moll10,Moll11,Moll12,Moll13,Moll14,Moll15,Moll16,Moll17,Moll18,Moll19,Moll20"
xOpts: ;;;;Mytilus edulis
yOpts: ;;;;Mytilus coruscus
caption: Oxford plot of Mytilus edulis and Mytilus coruscus using metazoa BUSCO genes
ratio: 1
result: feature
taxonomy: ncbi
xs: 4
```

```report
report: oxford
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type=metazoa_odb10-busco-gene AND busco_status!=duplicated AND ancestral_unit
queryA: assembly--tax_name(Mytilus edulis)
queryB: assembly--tax_name(Mytilisepta virgata)
cat: "ancestral_unit[20]=Moll1,Moll2,Moll3,Moll4,Moll5,Moll6,Moll7,Moll8,Moll9,Moll10,Moll11,Moll12,Moll13,Moll14,Moll15,Moll16,Moll17,Moll18,Moll19,Moll20"
xOpts: ;;;;Mytilus edulis
yOpts: ;;;;Mytilisepta virgata
caption: Oxford plot of Mytilus edulis and Mytilisepta virgata using metazoa BUSCO genes
ratio: 1
result: feature
taxonomy: ncbi
xs: 4
```

```report
report: oxford
x: assembly_id=queryA.assembly_id,queryB.assembly_id AND collate(sequence_id,busco_gene) AND feature_type=metazoa_odb10-busco-gene AND busco_status!=duplicated AND ancestral_unit
queryA: assembly--tax_name(Mytilus edulis)
queryB: assembly--tax_name(Crassostrea virginica)
cat: "ancestral_unit[20]=Moll1,Moll2,Moll3,Moll4,Moll5,Moll6,Moll7,Moll8,Moll9,Moll10,Moll11,Moll12,Moll13,Moll14,Moll15,Moll16,Moll17,Moll18,Moll19,Moll20"
xOpts: ;;;;Mytilus edulis
yOpts: ;;;;Crassostrea virginica
caption: Oxford plot of Mytilus edulis and Crassostrea virginica using metazoa BUSCO genes
ratio: 1
result: feature
taxonomy: ncbi
xs: 4
```

:::

BoaT provides templates to generate Oxford plots based on assembly accessions or taxon names, and color BUSCO loci by ancestral linkage groups.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/oxfordPlotByAssembly.md xs=6}

::include{pageId=templates/oxfordPlotByTaxon.md xs=6}

:::

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/oxfordPlotByAssemblyMollusca.md xs=6}

::include{pageId=templates/oxfordPlotByTaxonMollusca.md xs=6}

:::
