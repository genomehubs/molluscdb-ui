::valuerow{suffix="span" description="The total length of assembly {assemblyId} is {count} base pairs" value="attributes.assembly_span.value" unit=b}

::valuerow{suffix="level" description="Assembly {assemblyId} has been assembled to the {lc_attributes.assembly_level.value} level" value="attributes.assembly_level.value"}

::valuerow{suffix="chromosomes" description="Assembly {assemblyId} has {count} chromosomes" value="attributes.chromosome_count.value"}

::valuerow{condition="{attributes.assembly_level.value}=Chromosome" suffix="scaffolds" description="Assembly {assemblyId} has  {count} scaffolds" value="attributes.scaffold_count.value"}

::valuerow{condition="{attributes.assembly_level.value}=Chromosome" suffix="n50" description="The scaffold N50 of assembly {assemblyId} is {count}" value="attributes.scaffold_n50.value" unit=b}

::valuerow{condition="{attributes.assembly_level.value}=Contig,Scaffold" suffix="{lc_attributes.assembly_level.value}s" description="Assembly {assemblyId} has  {count} {lc_attributes.assembly_level.value}s" value="attributes.scaffold_count.value"}

::valuerow{condition="{attributes.assembly_level.value}=Contig,Scaffold" suffix="n50" description="The {lc_attributes.assembly_level.value} N50 of assembly {assemblyId} is {count}" value="attributes.scaffold_n50.value" unit=b}

::valuerow{suffix="BUSCO complete" description="Assembly {assemblyId} has a BUSCO {attributes.busco_lineage.value} completeness score of {count}" value="attributes.busco_completeness.value" unit=%}