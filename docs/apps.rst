.. _apps:

Applications
============

*Carousel users have access to a variety of applications. Simply upload your data, launch your analysis, and share with your collaborators!*

Anvi’o Pan-Genome
------------------------------

The `anvi'o <https://merenlab.org/software/anvio/>`_ software library was created by the Meren Lab to provide
an open-source, community-driven analysis and visualization platform for microbial ‘omics data.
This particular Carousel app is used to compare a set of microbial genomes using the anvi'o pangenome display.
To prepare a set of genomes for display with this app, first pre-processs them with the 
`nf-anvio-pangenome workflow <https://github.com/FredHutch/nf-anvio-pangenome>`_.
The two anvi'o database files created by that workflow can be directly uploaded to Carousel and visualized using this app.
The extensive anvi'o documentation produced by the Meren Lab includes an
`explanatory tutorial on pan-genome analysis <https://merenlab.org/2016/11/08/pangenomics-v2/>`_ which may be helpful
for understanding the display provided by this app.

Bacterial Operon Visualization
---------------------------------

When analyzing a collection of bacterial genomes, it can be useful to summarize which of the genomes contain a particular set of genes.
In particular, it can be useful to have a display which summarizes both (a) how similar the genomes are to each other alongside
(b) whether they contain a particular set of genes.The analysis pipeline which can be used to generate this information is called
BOFFO (Bacterial Operon Finder for Functional Organization). The inputs to this pipeline are (1) a list of genomes to analyze, and
(2) a collection of genes to align against those genomes. After running the BOFFO pipeline, this app can be used to visualize the
results in a single display which combines a genome similarity dendrogram with a table showing which genes are present.
In addition, this app provides the ability to customize the visual display and export a vector PDF which can be used to generate publication-quality figures.

Custom Figure (Plotly Express)
---------------------------------

Sometimes you just want to make a figure. One of the most widely used software libraries for making images out of data is Plotly.
Using a table of data as an input, this software can produce a large variety of displays. To make some of this functionality
available without needing to use the command line, this app will render data provided as a spreadsheet (in CSV format) using
the Plotly library. Simply select the columns which contain the data corresponding to the X-axis, Y-axis, etc., and the app
will display an interactive figure which the user can customize and even download.

Custom R/Shiny
--------------------

Render an `R/Shiny dashboard <https://shiny.rstudio.com/>`_ using custom code and private data.
Using this app, a user may render any sort of R/Shiny dashboard, including the use of other data files for importing data for visualization.
The R/Shiny app in Carousel supports many common R libraries for data manipulation and visualization, but please
`be in touch <mailto:hutchddatacore@fredhutch.org>`_ if you require additional libraries for your visualization.

Gene-Level Analysis of Metagenomes (GLAM) Browser
------------------------------------------------------------------------

The GLAM (Gene-Level Analysis of Metagenomes) Browser was created to allow scientists to interactively
explore the results of gene-level metagenomics analysis performed using the `geneshot <https://github.com/Golob-Minot/geneshot/wiki>`_
bioinformatics workflow for microbiome analysis.
After running `geneshot <https://github.com/Golob-Minot/geneshot/wiki>`_ (v0.9 or later), a file will be created in the output directory ending in ``.rdb``.
This file contains a compressed version of the output data which has been optimized for rapid visualization using the GLAM Browser.
Upload the ``.rdb`` file for any experiment to Carousel using this app, and you will be able to inspect the characteristics of every detected organism,
as well as their association with experimental parameters.
Selecting any individual gene group will show further details, including the taxonomic and functional assignments (if any) for the genes in that group.

GiG-Map (Genes in Genomes - Map)
------------------------------------------------

When trying to understand the biological context of a set of microbial protein-coding genes, it can be very helpful to understand the distribution of organisms which contain that coding sequence in their genome. One of the most useful characteristics used to differentiate those microbial genomes which do or do not contain a set of genes is their overall evolutionary history, for which taxonomic assignment is commonly used as a proxy. With this type of analysis it can become more easily evident when a set of genes are, for example, common to a cohesive taxonomic grouping (i.e. genus-, or species-specific), found sporadically across representatives within a taxonomic grouping (i.e. strain-specific), or found across disparate taxonomic groupings (i.e., horizontally transfered genes).

After running the ``gig-map`` alignment utility, a file will be created in the output directory ending in ``*.rdb``. This file contains a compressed version of the output data which has been optimized for rapid visualization.

Upload the ``*.rdb`` file for any experiment to Carousel using this app, and you will be able to inspect the detection of genes across genomes, as well as any addition annotations provided for genes and genomes.

For more details on how to generate these alignments, as well as the appropriate annotations, please reference the `gig-map repository <https://github.com/FredHutch/gig-map>`_ .

iSEE
---------

`iSEE package <https://github.com/iSEE/iSEE>`_ provides an interactive user interface for exploring data in objects derived from the SummarizedExperiment class. Explore data stored in SummarizedExperiment objects, including row- and column-level metadata. Once you are done generating plots, click on the export icon in the upper right corner, and click on the magic wand button to display R code that you can export and directly re-use in your R session! For a full description of the user interface read section 4 of the `iSEE user guide <https://bioconductor.org/packages/release/bioc/vignettes/iSEE/inst/doc/basic.html#4_Description_of_the_user_interface>`_

This application works best if you have saved PCA and TSNE information in your summarized experiment object. See the iSEE `user guide <https://bioconductor.org/packages/release/bioc/vignettes/iSEE/inst/doc/basic.html>`_ section 2 to learn how to best prepare your data.

The iSEE application expects a summarized experiement object saved in `rds file format <http://www.sthda.com/english/wiki/saving-data-into-r-data-format-rds-and-rdata>`_.

JBrowse2
-------------------

JBrowse2 is a pluggable open-source platform for visualizing and integrating biological data.
JBrowse2's most important feature is that it is able to compose multiple views of your data together on the same screen.
The JBrowse2 `website <https://jbrowse.org/jb2/>`_ contains extensive documentation, demos, and educational resources.
In order to display your data, JBrowse 2 requires (1) the reference genome for your organism of interest and
(2) a set of tracks that overlay additional information on that genome.

Pan-Epigenome Browser
-------------------------------

Bacteria contain an incredible amount of diversity regarding the epigenetic modifications contained in their genomes. These chemical modifications of nucleotides are much more varied than what has been described in eukaryotes, and they have been documented to confer enhanced fitness via a variety of mechanisms including defense from mobile genetic elements, regulation of genes, and the coordination of genome replication.

The Pan-Epigenome Browser allows researchers to compare a collection of bacterial isolates in terms of the epigenetic modifications which have been detected in those genomes via PacBio SMRT sequencing.

The input data for the Pan-Epigenome Browser must include the following for each genome:

- Epigenetic data from REBASE in text format (e.g. Genus_species_strain1.txt)
- Genome nucleotide sequence in FASTA format (e.g. Genus_species_strain1.fasta)
- Genome annotations in GBK format (e.g. Genus_species_strain1.gbk)
- Each of the three files for each genome must be named in the same way, except for the file extension, as shown above.

To most easily upload a group of files for many genomes, all of the files described above can be combined into a single ZIP file, and the browser will parse all of the contents of that ZIP file.

Additionally, annotations for the genomes and motifs can be provided in CSV format. For both of those annotation files, the genome name (e.g. 'Genus_species_strain1') (or motif sequence. e.g. 'GTAC') must be listed in the first column. Any additional annotations for those genomes (or motifs) can then be listed in the additional columns. Make sure to include a header row for all annotation files. The genome and motif annotations should be saved in separate files.

The display of the Pan-Epigenome Browser includes:

- A summary of which motifs are detected in which genomes.
- User-driven annotation of genomes and motifs
- Clustering of genomes and motifs by user-selected annotations, or by similarity of epigenetic profiles
- A detailed map of motif density across each genome, in the spatial context of annotations from GBK inputs
- Customization of figure size and orientation
- Export to static files for making figures

The Pan-Epigenome Browser was designed by Prof. Chris Johnston at Fred Hutch and built by the Fred Hutch Data Core. The code used to render the app can be found `here <https://github.com/fredhutch/panepigenomebrowser>`_.

R markdown
-------------------

Render an `R Markdown document <https://rmarkdown.rstudio.com/>`_ using custom code and private data.
If the R Markdown document is being used to display data which is contained in other data files,
just upload those additional files and reference them directly in your R Markdown code.

Single Cell Atlas (cellxgene)
------------------------------------------
  
The Chan-Zuckerberg Institute has created an interactive data explorer for single-cell transcriptomics called
cellxgene (pronounced "cell-by-gene"). The cellxgene `website <https://github.com/chanzuckerberg/cellxgene>`_ contains documentation on how to prepare your data for display.
Once you have prepared the .h5ad file required by cellxgene, upload it to Carousel for display using this app.

Streamlit
--------------

Streamlit is a flexible Python library for rendering interactive datasets with convenient options for building user interaction through menus and sliders.

To load your Streamlit apps in Carousel, simply provide the file containing all of the Python code used to render the app, as well as any additional data files which are needed by that script. Any additional data files will be made available to access from the working directory when the app is launched.

For a more extensive description of how to use Streamlit, visit `their documentation <https://streamlit.io/>`_ or browse the `example gallery <https://streamlit.io/gallery>`_.

Request an application
---------------------------------

We are always looking to add new visualizations and analyses to Carousel.
Any open-source visualization tool that is compatible with Docker can be added to Carousel.

Put more simply the tool needs to be:  

- Free
- Able to run on Linux
- Have an interactive visualization component

If you are unsure if a tool is right for Carousel don’t hesitate to `contact us! <mailto:hutchdatacore@fredhutch.org>`_