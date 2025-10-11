UPPMAX
=====

Getting access
------------

Logging in and transferring files
------------

Running pipelines
------------
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

