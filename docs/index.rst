.. Carousel documentation master file, created by
   sphinx-quickstart on Thu Jul 22 09:23:21 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

===================================
Carousel: Share Interactive Data
===================================

*Carousel is a web platform for uploading and sharing interactive datasets.*

Scientific research is founded on the idea that we can better understand the world by carefully
collecting data and building falsifiable models which explain those data. While modern technology has
played a large role in breakthrough scientific discoveries, the human brain is still the most powerful
tool at our disposal for recognizing patterns and guessing at the underlying generative systems. Carousel
helps researchers access a richer comprehension of complex datasets by providing interactive displays
developed by other scientists to illuminate the patterns which make up the physical world.

One Portal, Many Visualizations
------------------------------------

It has never been easier for researchers to design and build data visualization tools tuned to their
exact type of data. With tools like `Shiny <https://shiny.rstudio.com/>`_ , `Dash<https://plotly.com/dash/>`_,
and `Streamlit<https://streamlit.io>`_, simple scripts in R or Python can be transformed into dashboards
with interactive menus and displays which can be explored in endless combinations. Even more powerful
and sophisticated tools (like `anvi'o<https://merenlab.org/software/anvio/>`_, `JBrowse<https://jbrowse.org/jb2/`>_,
and `cellxgene<https://github.com/chanzuckerberg/cellxgene>`_) are being built by computational biologists
to provide intuitive understanding of extremely complex datasets.

While it has become much easier for researchers to generate interactive visualizations of custom data,
it is still difficult to share those visualizations with collaborators and the larger scientific community.
While some of the tools above come with websites for sharing, most of those options are specific to a single
language or codebase. In contrast, Carousel provides compatibility across all visualization tools. By
using `Docker<https://www.docker.com/>`_ as the fundamental building block for rendering visualizations,
Carousel aims to unlock the full creative potential of the scientific community by allowing scientists
to innovate with complete flexibility.

Using Carousel
-----------------

Using Carousel, users can:

- Upload their own datasets, simply providing the files which are needed to run a particular visualization tool
- Launch visualizations, without the need to install any software
- Share datasets directly with collaborators, quickly providing access without having to transfer large files

Users interact with Carousel as a website. Each account is password protected and consists of their personal
datasets, each of which is linked to an app. Once a dataset is uploaded you are able to launch your
visualization and share with collaborators directly through the platform. Using Carousel, users get to
skip any command line installation and processing steps required of many open-source tools. Simply select
your desired application, upload the relevant data, and view your data interactively! Easily share your
interactive datasets and visualizations through the platform with other users.

Work In Progress
--------------------

Carousel is under active development by the Fred Hutch Data Core - if you notice that anything is out of date or
broken, please `contact us<mailto:hutchdatacore@fredhutch.org>`_!

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   getting_started
   apps
