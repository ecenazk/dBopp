## Synteny Plot
The script here is used for the Master's Project I've been involved in Bopp Lab of University of Zurich.
Comparing the genomic positions of orthologs on two or more genomes, it is possible to infer the synteny between them. For visualizing these syntenies, there exist several plotting tools. Here, we use the R package RIdeogram (Hao et al., 2020) for this job, in a script inspired by the support protocol of a paper explaining a way to visualize BUSCO results (Manni et al., 2021). Our script first creates a synteny map between the given two species by merging the location information of orthologous by their orthologous group. Then, the karyotype data of the two species are gathered in a single file. From this point, the synteny data variables are converted fully to integers and fed into RIdeogram, which produces an SVG file that is then converted to the depiction of a plot. In the plot, both karyotypes of the two species are shown, with homologs mapped by lines to connect each other. As the two species can be any two species with related and known orthologs, any database or orthologs can be used. To date, we have used OrthoDB orthologs (http://www.orthodb.org) and OrthoMCL DB (https://orthomcl.org/orthomcl) orthologs, former cataloging groups of single-copy orthologous genes hierarchically by taxon, latter grouping orthologous protein sequences between two or more species.
