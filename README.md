conda install -c bioconda nanoplot

NanoPlot --fastq SRR17041451.fastq -f png --outdir SRR17041451
Common threshold for longreads is Q7 to Q9 corresponds to error rate of ~20%-10% 
-> using nanofilt to trim seq below Phred's score of q9 and shorter than 1000 bases 
cat SRR17041451.fastq | NanoFilt -q 7 -l 1000 | gzip > trimmed_SRR17041451.fastq.gz

