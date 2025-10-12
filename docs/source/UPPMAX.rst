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
      subgraph cluster0 {
         node [style=filled,color=white];
         style=filled;
         color=lightgrey;
         "anat" [shape=box];
         "dwi" [shape=box];
         "fmri" [shape=box];
         label = "raw data";
      }
      subgraph cluster1 {
         "anat" -> "mriqc";
         "dwi" -> "mriqc";
         "fmri" -> "mriqc";
         "fmri" -> "fmriprep";
         "anat" -> "fmriprep";
         "anat" -> "qsiprep";
         "anat" -> "freesurfer";
         "dwi" -> "qsiprep";
         "qsiprep" -> "qsirecon";
         subgraph cluster2 {
            "fmriprep" -> "xcp_d";
            label = "rs-fmri";
         }
         "freesurfer" -> "fmriprep";
         "freesurfer" -> "qsirecon";
         subgraph cluster3 {
            "fmriprep" -> "fitlins";
            label = "task-fmri";
         }
         label = "processing pipelines";
      }
   }

