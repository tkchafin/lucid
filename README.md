# lucid
long-read ultra-conserved integrated DNA assembler

## Temporary pipeline 

### Filtering
* Trim Q from edges, filter by Q (NanoPack)
* Remove DNA CS (Nanopack)
* Remove adapters (Vanilla porechop)
* Remove illumina adapters and place in headers (LR-UCE_Porechop)
python3 LR-UCE_Porechop/porechop-runner.py -i lr_uce_noCS_chop_filt-q10.fastq --skip_barcodes --write_adapters --exclude_untrimmed -o tlr_uce_noCS_chop_filt-q10_ILL.fastq
* Sort by barcode (LR-UCE_Porechop)



### Demultiplexing/ error rates
* Trim off Illumina adapters - use to estimate per-base error rates
* Sort reads by barcode

### Locus Assembly 
* Clustering by VSEARCH 
* Alignment, clustalo or muscle, etc 
* End trim alignments by per-base coverage (i.e. 10X minimum)
