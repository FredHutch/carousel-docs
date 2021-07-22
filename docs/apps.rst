Applications
=========

*Carousel users have access to a variety of applications. Simply upload your data, launch your analysis, and share with your collaborators!*

R markdown
**************

Render an `R Markdown document <https://rmarkdown.rstudio.com/>`_ using custom code and private data.
If the R Markdown document is being used to display data which is contained in other data files,
just upload those additional files and reference them directly in your R Markdown code.

 Custom R/Shiny
*****************

Render an `R/Shiny dashboard <https://shiny.rstudio.com/>`_ using custom code and private data.
Using this app, a user may render any sort of R/Shiny dashboard, including the use of other data files for importing data for visualization.
The R/Shiny app in Carousel supports many common R libraries for data manipulation and visualization, but please
`be in touch <mailto:hutchddatacore@fredhutch.org>`_ if you require additional libraries for your visualization.

 Anvi’o Pan-Genome
 *********************



The `anvi'o <https://merenlab.org/software/anvio/>`_ software library was created by the Meren Lab to provide
an open-source, community-driven analysis and visualization platform for microbial ‘omics data.
This particular Carousel app is used to compare a set of microbial genomes using the anvi'o pangenome display.
To prepare a set of genomes for display with this app, first pre-processs them with the 
`nf-anvio-pangenome workflow <https://github.com/FredHutch/nf-anvio-pangenome>`_.
The two anvi'o database files created by that workflow can be directly uploaded to Carousel and visualized using this app.
The extensive anvi'o documentation produced by the Meren Lab includes an
`explanatory tutorial on pan-genome analysis <https://merenlab.org/2016/11/08/pangenomics-v2/>`_ which may be helpful
for understanding the display provided by this app.

 JBrowse2
************

`JBrowse2 <https://jbrowse.org/jb2>`_ is a pluggable open-source platform for visualizing and integrating biological data.
JBrowse2's most important feature is that it is able to compose multiple views of your data together on the same screen.
The JBrowse2 `website <https://jbrowse.org/jb2/>`_ contains extensive documentation, demos, and educational resources.
In order to display your data, JBrowse 2 requires (1) the reference genome for your organism of interest and
(2) a set of tracks that overlay additional information on that genome.

 Single Cell Atlas (cellxgene)
 ******************************
  
The Chan-Zuckerberg Institute has created an interactive data explorer for single-cell transcriptomics called
`cellxgene <https://github.com/chanzuckerberg/cellxgene>`_ (pronounced "cell-by-gene"). The cellxgene 
`website <https://github.com/chanzuckerberg/cellxgene>`_ contains documentation on how to prepare your data for display.
Once you have prepared the .h5ad file required by cellxgene, upload it to Carousel for display using this app.

 Gene-Level Analysis of Metagenomes (GLAM) Browser
 ---------------------------------------------------------

The GLAM (Gene-Level Analysis of Metagenomes) Browser was created to allow scientists to interactively
explore the results of gene-level metagenomics analysis performed using the `geneshot <https://github.com/Golob-Minot/geneshot/wiki>`_
bioinformatics workflow for microbiome analysis.
After running `geneshot <https://github.com/Golob-Minot/geneshot/wiki>`_ (v0.9 or later), a file will be created in the output directory ending in `.rdb`.
This file contains a compressed version of the output data which has been optimized for rapid visualization using the GLAM Browser.
Upload the `.rdb` file for any experiment to Carousel using this app, and you will be able to inspect the characteristics of every detected organism,
as well as their association with experimental parameters.
Selecting any individual gene group will show further details, including the taxonomic and functional assignments (if any) for the genes in that group.

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

 Request an application
 ---------------------------------
We are always looking to add new visualizations and analyses to Carousel.
Any open-source visualization tool that is compatible with Docker can be added to Carousel.

Put more simply the tool needs to be:  

- Free
- Able to run on Linux
- Have an interactive visualization component

If you are unsure if a tool is right for Carousel don’t hesitate to `contact us! <mailto:hutchdatacore@fredhutch.org>`_