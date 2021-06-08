# Shim et al (2021)

This repository contains the information and scripts for analysis in [Shim et al. (2021)][multiseq-arxiv] and their results.  

  * [The main manuscript and supplementary material][multiseq-arxiv]
  * [the multiseq R package][multiseq-package] and [its vignette][multiseq-web].
  * ATAC-seq data (hdf5 format) for nine samples can be downloaded from [this link][ATAC-seq-hdf5]. These files have been converted from bam files using this script. 
4.	ATAC-seq analysis 
Information on the 242,714 regions included in the analysis (the top 5% of regions with the highest chromatin accessibility) and results from the analysis are in XXX
A script to for each region 1) extract ATAC-seq count data at the region on 6 samples (6 by 1024) from the hdf5 files and 2) do data-  preprocessing as described in Shim et al (2021) is in /
Once you have the count data after data-processing, you can follow the vignette of the multiseq R package to 1) run multiseq, and 2) plot estimated effect sizes as shown in Shim et al (2021).
5.	Simulation procedure described in Shim et al (2021) has been implemented in the function of the multiseq R package. See the vignette of the multiseq R package to see how to use this function. 


## License

Copyright (c) 2021-2023, Heejung Shim

All source code and software in this repository is free software; you
can redistribute it and/or modify it under the terms of the
[GNU General Public License][gpl] as published by the
[Free Software Foundation][fsf]; either version 3 of the License, or
(at your option) any later version. See the [LICENSE](LICENSE) file
for the full text of the license.


[multiseq-arxiv]: XXX
[gpl]: http://www.gnu.org/licenses/gpl.html
[fsf]: https://www.fsf.org
[multiseq-web]: https://heejungshim.github.io/multiseq
[multiseq-package]: https://github.com/heejungshim/multiseq 
[ATAC-seq-hdf5]: XXX

