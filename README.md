# lucid
long-read ultra-conserved integrated DNA assembler

## To-do 

### Filtering
* Remove adapters (or use porechop?) 
* Trim by Q from edges
* Remove reads by mean Q
* Min/max length
* Remove DNA CS 

### Demultiplexing/ error rates
* Trim off Illumina adapters - use to estimate per-base error rates
* Sort reads by barcode

### Locus Assembly 
* Clustering by VSEARCH 
* Alignment, clustalo or muscle, etc 
* End trim alignments by per-base coverage (i.e. 10X minimum)
