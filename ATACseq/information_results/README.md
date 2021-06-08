This directory contains information on ATAC-seq analysis in Shim et al 2021 and results from the analysis. 

  * `Copper.1024.info.results` provides, for each of the 242,714 regions, location information (`chr`, `st.posi`, `en.posi`), q-values for multiseq, WaveQTL, and DESeq2 with different bin sizes (`qval.multiseq`, `qval.WaveQTL`, `qval.DESeq2.100`, `qval.DESeq2.300`, `qval.DESeq2.1024`), p-values from empirical null distribution for multiseq, WaveQTL, and DESeq2 with different bin sizes (`pval.multiseq`, `pval.WaveQTL`, `pval.DESeq2.100`, `pval.DESeq2.300`, `pval.DESeq2.1024`), log likelihood test statistic for multiseq from copper treatment vs. control 1 (`logLR.multiseq`) and control 1 vs. control 2 (`logLR.multiseq.null`), and log likelihood test statistic for DESeq22 with 1024bp from copper treatment vs. control 1 (`logLR.DESeq2.1024`) and control 1 vs. control 2 (`logLR.DESeq2.1024.null`). 
  
  * `Copper.prob` contains sampling probabilities for 6 samples (copper treatment vs control 1) which are used in [subsampling](https://github.com/heejungshim/multiseq_Shim_et_al/blob/main/scripts/ATAC-seq.Rmd).
  
  * `Copper.null.prob` contains sampling probabilities for 6 samples (control 2 vs control 1) which are used in th subsampling. 
  
  * `library.read.depth.fwd.Copper` and `library.read.depth.rev.Copper` contains expected library read depths for 6 samples (copper treatment vs control 1) after [subsampling](https://github.com/heejungshim/multiseq_Shim_et_al/blob/main/scripts/ATAC-seq.Rmd).
  
  * `library.read.depth.fwd.Copper.null` and `library.read.depth.rev.Copper.null` contains expected library read depths for 6 samples (control 2 vs control 1) after subsampling.
  
  