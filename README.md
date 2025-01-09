# Code and resources relating to our manuscript "Characterizing the expression profile of 3R tau pathology in Pick’s disease"

## Short-read bulk RNA Sequencing https://github.com/ORossLab/Picks_Bulk_RNASeq/blob/main/README.md

The script used for data clean up, quality control, normalization using CQN, and differential gene expression analysis can be found here in the "Bulk Short-read RNASeq Analysis Script" tab.\
The script used for WGCNA can be found in the "WGCNA_analysis" tab.

## Long-read bulk RNA Sequenicng 

For long-read RNA Sequencing analysis we used scripts and resources available through the PacBio github page at:
* https://github.com/PacificBiosciences
* https://github.com/PacificBiosciences/ccs
* https://ccs.how/
* https://github.com/PacificBiosciences/IsoSeq
* https://isoseq.how/clustering/cli-workflow.html

Please note that some of the versions of scripts and programs available through PacBio might be available different versions that what was used for this study.\
In brief, we first generated CCS reads from the subreads.bam files for each sample using the following parameters:\
-min-passes 3 --min-snr 2.5 --min-length 10 --max-length 50000 --min-rq 0.9\

Then we performed primer removal using lima and refined by trimming poly(A) tails and removing concatemers using the isoseq3 refine command.\

Then we employed flair, documentation for which can be accessed here:\
* https://github.com/BrooksLabUCSC/flair\




## Validating transcripts identified with long-read sequencing using short-read sequencing data and Kallisto

We used a custom annotation file where we added the sequences of our novel transcripts of interest. This file can be accessed in our Github "gencode.v44.transcripts.enriched.fa.gz". \ 
For Kallisto, we used the documentation available here:
* https://pachterlab.github.io/kallisto/about
* https://github.com/pachterlab/kallisto



