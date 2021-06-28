# Shim et al (2021)

This repository contains the information and scripts for analysis in [Shim et al. (2021)][multiseq-arxiv] and their results.  

  * [The main manuscript and supplementary material](https://github.com/heejungshim/multiseq_Shim_et_al/tree/main/manuscript)
  * [the multiseq R package][multiseq-package] and [its vignette][multiseq-web].
  * ATAC-seq data (hdf5 format) for nine samples can be downloaded from [this link][ATAC-seq-hdf5]. These files have been converted from bam files using a script in [multiseq_Shim_et_al/scripts/bamTOhdf5.md](https://github.com/heejungshim/multiseq_Shim_et_al/tree/main/scripts/bamTOhdf5.md).
  * ATAC-seq analysis 
      1. Information on the 242,714 regions included in the analysis (the top 5% of regions with the highest chromatin accessibility) and results from the analysis are in [multiseq_Shim_et_al/ATACseq/information_results](https://github.com/heejungshim/multiseq_Shim_et_al/tree/main/ATACseq/information_results).
      2. A script to for each region 1) extract ATAC-seq count data at the region on 6 samples (6 by 1024) from the hdf5 files and 2) do data-preprocessing as described in Shim et al (2021) is in [multiseq_Shim_et_al/scripts/ATAC-seq.Rmd](https://github.com/heejungshim/multiseq_Shim_et_al/tree/main/scripts/ATAC-seq.Rmd).
      3. Once we have the count data after the data-preprocessing, we can follow [the vignette of the multiseq R package][multiseq-web] to 1) run multiseq, and 2) plot estimated effect sizes as shown in Shim et al (2021).
  * Simulation procedure described in Shim et al (2021) has been implemented in the function `sample.from.Binomial.with.Overdispersion` of [the multiseq R package][multiseq-package]. See [the vignette of the multiseq R package][multiseq-web] to see how to use this function. 


## License

Copyright (c) 2021-2023, Heejung Shim

All source code and software in this repository is free software; you
can redistribute it and/or modify it under the terms of the
[GNU General Public License][gpl] as published by the
[Free Software Foundation][fsf]; either version 3 of the License, or
(at your option) any later version. See the [LICENSE](LICENSE) file
for the full text of the license.


[multiseq-arxiv]: https://arxiv.org/abs/2106.13634
[gpl]: http://www.gnu.org/licenses/gpl.html
[fsf]: https://www.fsf.org
[multiseq-web]: https://heejungshim.github.io/multiseq
[multiseq-package]: https://github.com/heejungshim/multiseq 
[ATAC-seq-hdf5]: https://melbourne.figshare.com/articles/dataset/ATAC-seq_data_from_Shim_et_al_2021/14748480

