::phylopic{recordId="{assembly_id}"}

::recordlink{result=taxon rank=species url="https://goat.genomehubs.org/record?recordId={taxon_id}&result=taxon" label="GoaT" color=#31323f description="Click to view in Genomes on a Tree" icon="https://goat.genomehubs.org/apple-touch-icon.png"}

::recordlink{result=assembly rank=species url="https://goat.genomehubs.org/record?recordId={assembly_id}&result=assembly" label="GoaT" color=#31323f description="Click to view in Genomes on a Tree" icon="https://goat.genomehubs.org/apple-touch-icon.png"}

::recordlink{result=assembly rank=species url="https://boat.genomehubs.org/record?recordId={identifiers[class:boat_id].identifier}&result=assembly" condition="identifiers[class:boat_id]" label="BoaT" color=#31323f description="Click to view in BoaT" icon="https://boat.genomehubs.org/apple-touch-icon.png"}

::recordlink{result=taxon rank=species url="https://portal.darwintreeoflife.org/data/root/details/{scientific_name}" condition="attributes.bioproject=PRJEB40665" label="Darwin portal" color=#8fbc45 description="Click to view in the Darwin Tree of Life Data Portal"}

::recordlink{result=assembly url="https://portal.darwintreeoflife.org/data/organism/details/{attributes.biosample.value}" condition="attributes.bioproject=PRJEB40665" label="Darwin portal" color=#8fbc45 description="Click to view in the Darwin Tree of Life Data Portal"}

::recordlink{result=taxon url="https://blobtoolkit.genomehubs.org/view/{taxon_id}" condition="attributes.btk_target" label="BlobToolKit" color=#9c528b description="Click to view in the BlobToolKit Viewer"}

::recordlink{result=assembly url="https://blobtoolkit.genomehubs.org/view/{assemblyId}" condition="attributes.btk_target" label="BlobToolKit" color=#9c528b description="Click to view in the BlobToolKit Viewer"}

::recordlink{result=taxon,assembly url="https://www.ebi.ac.uk/ena/browser/view/{assemblyId}" condition="assemblyId" label="ENA" color=#70bdbd description="Click to view the primary assembly {assemblyId} in ENA"}

::recordlink{result=taxon,assembly url="https://www.ncbi.nlm.nih.gov/assembly/{assemblyId}" condition="assemblyId" label="NCBI" color=#20558a description="Click to view the primary assembly {assemblyId} in NCBI"}

::recordlink{result=taxon,assembly url="https://genome.ucsc.edu/h/{identifiers[class:ucsc_id].identifier}" condition="identifiers[class:ucsc_id]" label="UCSC" color=#D4A017 description="Click to view the primary assembly {assemblyId} in the UCSC Genome Browser"}

::recordlink{result=assembly url="https://metazoa.ensembl.org/{identifiers[class:ensembl_metazoa_id].identifier}/Info/Index" condition="identifiers[class:ensembl_metazoa_id]" label="Ensembl Metazoa" color=#015365 description="Click to view the primary assembly {assemblyId} in the Ensembl Metazoa Genome Browser"}

::recordlink{result=assembly url="https://rapid.ensembl.org/{identifiers[class:ensembl_rapid_id].identifier}/Info/Index" condition="identifiers[class:ensembl_rapid_id]" label="Ensembl Rapid" color=#2378a9 description="Click to view the primary assembly {assemblyId} in the Ensembl Rapid Genome Browser"}
