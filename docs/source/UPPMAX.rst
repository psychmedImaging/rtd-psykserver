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
      "anat" -> "mriqc";
      "dwi" -> "mriqc";
      "fmri" -> "mriqc";
      "fmri" -> "fmriprep";
      "anat" -> "fmriprep";
      "anat" -> "qsiprep";
      "anat" -> "freesurfer";
      "dwi" -> "qsiprep";
      "qsiprep" -> "qsirecon";
      "fmriprep" -> "xcp_d";
      "freesurfer" -> "fmriprep";
      "freesurfer" -> "qsirecon";
      "fmriprep" -> "fitlins";
   }

