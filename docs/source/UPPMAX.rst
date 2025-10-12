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
      "fmri" -> "fmriprep";
      "anat" -> "fmriprep";
      "anat" -> "qsiprep";
      "anat" -> "freesurfer";
      "dwi" -> "qsiprep";
      "qsiprep" -> "qsirecon";
      "fmriprep" -> "xcp_d";
      "freesurfer" -> "fmriprep";
      "freesurfer" -> "qsirecon";
   }

