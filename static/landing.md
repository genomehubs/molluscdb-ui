# Explore MolluscDB data

:::grid{container direction="row" spacing="1"}

::include{pageId=data-summary.md size=8 className=unpadded}

```report
report: xPerRank
x: mollusca_odb10_complete
includeEstimates: true
result: taxon
taxonomy: ncbi
rank: order,family,genus,species
size: 4
caption: Numbers of taxa available on MolluscDB
```

:::

:::grid{container direction="row" spacing="1"}

```report
report: scatter
x: "midpoint AND assembly_id=GCA_007844125.1 AND feature_type=mollusca_odb10-busco-gene AND busco_status!=duplicated AND ancestral_unit"
y: sequence_id
cat: "ancestral_unit[20]=moll1,moll2,moll3,moll4,moll5,moll6,moll7,moll8,moll9,moll10,moll11,moll12,moll13,moll14,moll15,moll16,moll17,moll18,moll19,moll20"
includeEstimates: false
xOpts: ";;;linear"
yOpts: "nsort;;15"
scatterThreshold: -1
result: feature
taxonomy: ncbi
size: 12
ratio: 2
colorPalette: plasma:20
caption: "BUSCO painting of Sinonovacula constricta chromosomes showing assignments of each BUSCO locus to the 20 molluscan ancestral linkage groups"
```

:::

:::grid{container direction="row" spacing="1"}

MolluscDB uses [BUSCO](https://busco.ezlab.org) data to infer orthology between loci across assemblies. These loci are also used in the ancestral linkage group assessment. Many mollusc assemlies have lower scores than observed for assemblies using similar technologies in other lineages. Comparison between results using the mollusca_odb10 and metazoa_odb10 lineages can help to highlight assemblies where the lower score may be an artifact rather than a true reflection of relative assembly quality.

```report
report: arc
x: mollusca_odb10_complete_percent>85
y: mollusca_odb10_complete
includeEstimates: true
result: assembly
taxonomy: ncbi
size: 4
caption: Proportion of genome assemblies on MolluscDB with BUSCO completeness above 80% (BUSCOv5; mollusca_odb10)
```

```report
report: scatter
x: metazoa_odb10_complete_percent AND tax_tree(6447[Mollusca]) AND mollusca_odb10_complete_percent
y: mollusca_odb10_complete_percent
cat: class[6]
xOpts: 60;100;9;;metazoa_odb10 complete BUSCOs
yOpts: 60;100;9;;mollusca_odb10 complete BUSCOs
scatterThreshold: -1
result: assembly
taxonomy: ncbi
highlightArea: y=x
ratio: 2.25
size: 8
caption: Relative counts of Metazoa and Mollusca BUSCOs for assemblies on MolluscDB
```

_All plots on MolluscDB are interactive, click on the plots above to search within a bin or click the icon to the top right of each plot to expand and view more options._

:::

:::grid{container direction="row" toggle title="Taxonomic distribution of BUSCO scores" spacing="1" class="padded"}

```report
report: tree
x: tax_tree(6447[Mollusca]) AND tax_rank(order)
y: mollusca_odb10_complete_percent
levels: species,order
includeEstimates: true
collapseMonotypic: true
yOpts: 50,100
pointSize: 15
result: taxon
caption: |
  Tree showing BUSCO completeness of taxa in MolluscDB
  based on analyses using the mollusca_odb10 lineage
ratio: 2.4
size: 12
```

```report
report: tree
x: tax_tree(6447[Mollusca]) AND tax_rank(order)
y: metazoa_odb10_complete_percent
levels: species,order
includeEstimates: true
collapseMonotypic: true
yOpts: 50,100
pointSize: 15
result: taxon
caption: |
  Tree showing BUSCO completeness of taxa in MolluscDB
  based on analyses using the metazoa_odb10 lineage
ratio: 2.4
size: 12
```

:::

## Search templates

We have created a set of advanced search templates to highlight some of the ways to explore the data in MolluscDB. The templates below can be used to generate an oxford plot to compare assemblies of two taxa and to plot assembly metrics in windows along each chromosome of an assembly.

Visit the [templates page](/templates) for more examples.

:::grid{container direction="row" spacing="1"}

::include{pageId=templates/oxfordPlotByTaxon.md size=6 className=unpadded}

::include{pageId=templates/windowPlotByTaxon.md size=6 className=unpadded}

::grid[&nbsp;&nbsp;more [oxford plot templates](/templates/oxford)]{size=6}
::grid[&nbsp;&nbsp;more [window-based templates](/templates/windows)]{size=6}

:::

## Oxford plots

:hub allows exploration of colineraity between pairs of assemblies through Oxford plots using BUSCO gene positions.

:::grid{container direction="row" toggle title="Oxford plot examples" spacing="1" class="padded"}

```report
report: oxford
x: assembly_id=GCA_963676685.2,GCA_017311375.1 AND collate(sequence_id,busco_gene) AND feature_type=metazoa_odb10-busco-gene AND busco_status!=duplicated
ratio: 1.5
pointSize: 20
result: feature
size: 6
compactWidth: 900
caption: Oxford plot comparing Metazoa BUSCO genes between two bivalve assemblies,assemblies
```

```report
report: oxford
x: assembly_id=GCA_963676685.2,GCA_017311375.1 AND collate(sequence_id,busco_gene) AND feature_type=lepidoptera-busco-gene AND sequence_id = LR989906.1,LR990085.1,LR989907.1,LR990083.1
cat: ancestral_unit
colorPalette: pride
ratio: 1.5
pointSize: 20
result: feature
size: 6
caption: Detailed view of an oxford plot, coloured by ancestral linkage group, highlighting colinearity on two pairs of chromosomes
```

::grid{size=8}
::grid[&nbsp;&nbsp;more [examples and templates](/templates/oxford)]{size=4}

:::

## BUSCO counts

Busco identities are recorded for each taxon, allowing plots of BUSCO counts against other assembly metrics.

:::grid{container direction="row" toggle title="BUSCO counts" spacing="1" class="padded"}

```report
report: scatter
x: tax_tree(eukaryota) AND assembly_span AND mollusca_odb10_complete
y: mollusca_odb10_complete_percent
rank: species
cat: class[6]
includeEstimates: false
scatterThreshold: -1
result: taxon
taxonomy: ncbi
size: 12
ratio: 2
caption: Mollusca BUSCO counts against assembly span for the classes represented in MolluscDB
```

::grid{size=8}
::grid[&nbsp;&nbsp;more [examples and templates](/templates/counts)]{size=4}

:::
