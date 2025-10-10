psykserv documentation
===================================

Here you will find the necessary documentation to perform BIDS conversion of collected data and run BIDS compliant pipelines on UPPMAX.

.. note::

   This documentation is in alpha state.

Contents
--------

.. toctree::

   BIDS
   UPPMAX

.. graphviz::

   digraph {
      "anat" [shape=box];
      "dwi" [shape=box];
      "fmri" [shape=box];
      "anat" -> "fmriprep";
      "anat" -> "qsiprep";
      "fmri" -> "fmriprep";
      "dwi" -> "qsiprep";
      "qsiprep" -> "qsirecon";
      "fmriprep" -> "xcp_d";
   }
