We used a Python library, *genome* from https://github.com/gmcvicker/genome.

* Filtered reads with low alignment quality 10 and saved them at @process_bams:

```{}
samtools view -b -q 10 AT2-N702N501.bam > @process_bams/AT2-N702N501.qfiltered10.bam
samtools view -b -q 10 AT2-N702N502.bam > @process_bams/AT2-N702N502.qfiltered10.bam
samtools view -b -q 10 AT2-N702N503.bam > @process_bams/AT2-N702N503.qfiltered10.bam

samtools view -b -q 10 AT2-N705N501.bam > @process_bams/AT2-N705N501.qfiltered10.bam
samtools view -b -q 10 AT2-N705N502.bam > @process_bams/AT2-N705N502.qfiltered10.bam
samtools view -b -q 10 AT2-N705N503.bam > @process_bams/AT2-N705N503.qfiltered10.bam

samtools view -b -q 10 AT2-N706N501.bam > @process_bams/AT2-N706N501.qfiltered10.bam
samtools view -b -q 10 AT2-N706N502.bam > @process_bams/AT2-N706N502.qfiltered10.bam
samtools view -b -q 10 AT2-N706N503.bam > @process_bams/AT2-N706N503.qfiltered10.bam
```

* At @process_bams, index filtered bam files:

```{}
samtools index AT2-N702N501.qfiltered10.bam
samtools index AT2-N702N502.qfiltered10.bam
samtools index AT2-N702N503.qfiltered10.bam

samtools index AT2-N705N501.qfiltered10.bam
samtools index AT2-N705N502.qfiltered10.bam
samtools index AT2-N705N503.qfiltered10.bam

samtools index AT2-N706N501.qfiltered10.bam
samtools index AT2-N706N502.qfiltered10.bam
samtools index AT2-N706N503.qfiltered10.bam
```

* In ~/genome/python/script/db, convert the filtered bam files into hdf5 and save them at @ATAC_hdf5

python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N702N501.qfiltered10.fwd @ATAC_hdf5/N702N501.qfiltered10.rev @process_bams/AT2-N702N501.qfiltered10.bam
python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N702N502.qfiltered10.fwd @ATAC_hdf5/N702N502.qfiltered10.rev @process_bams/AT2-N702N502.qfiltered10.bam
python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N702N503.qfiltered10.fwd @ATAC_hdf5/N702N503.qfiltered10.rev @process_bams/AT2-N702N503.qfiltered10.bam

python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N705N501.qfiltered10.fwd @ATAC_hdf5/N705N501.qfiltered10.rev @process_bams/AT2-N705N501.qfiltered10.bam
python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N705N502.qfiltered10.fwd @ATAC_hdf5/N705N502.qfiltered10.rev @process_bams/AT2-N705N502.qfiltered10.bam
python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N705N503.qfiltered10.fwd @ATAC_hdf5/N705N503.qfiltered10.rev @process_bams/AT2-N705N503.qfiltered10.bam

python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N706N501.qfiltered10.fwd @ATAC_hdf5/N706N501.qfiltered10.rev @process_bams/AT2-N706N501.qfiltered10.bam
python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N706N502.qfiltered10.fwd @ATAC_hdf5/N706N502.qfiltered10.rev @process_bams/AT2-N706N502.qfiltered10.bam
python load_bam_5prime_ends.py --assembly hg19 @ATAC_hdf5/N706N503.qfiltered10.fwd @ATAC_hdf5/N706N503.qfiltered10.rev @process_bams/AT2-N706N503.qfiltered10.bam
