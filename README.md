# BacARscan: an in-silico resource to discern diversity in antibiotic resistance genes

Bacterial Antibiotic Resistance scan (BacARscan)(http://proteininformatics.org/mkumar/bacarscan/) that can detect, predict and characterize ARGs in -omics datasets, including short sequencing, reads, and fragmented contigs. Benchmarking on an independent non-redundant data set revealed that the performance of BacARscan was better than
other existing methods with ca. 92% precision and 95% F-measure on a combined dataset of ARG and nonARG proteins. One of the most notable improvements of BacARscan over other ARG annotation methods is its ability to work on genomes and small reads sequence libraries with equal efficiency and without any requirement for assembly of short reads. Thus, BacARscan can be helpful in monitoring the prevalence and diversity of ARGs in microbial populations and metagenomics samples from animal, human and environmental settings. 

***********How to use it? **************

######Files description#####

nARGhmm: Library of 254 nucleotide ARG HMMs

pARGhmm: Library of 254 protein ARG HMMs
ARG_Annotations: Annotation of 254 profile ARG HMMs

HMMER download and install as standalone using link: http://hmmer.org/download.html

*****Scanning of protein sequences will perform using hmmscan*****

“/hmmer-3.1b2-linux-intel-x86_64/src/hmmscan --cpu 4 -E 0.000001 --tblout abc.out pARGhmm protein.fasta”


****Scanning of gene sequences will perform using nhmmscan******

/hmmer-3.1b2-linux-intel-x86_64/src/nhmmscan --cpu 4 -E 0.000001 --tblout abc.out nARGhmm gene.fasta &


Using above commands user can scan their protein and nucleotide sequences; upon search it will give the similarity score and e-value. Depending on the scores user can select hits and retrieve their complete annotation using “ARG_Annotations” file.


Visit our website for latest version, Executable versions, source code, profile HMMs, annotations, seed sequences and usage instructions can be downloaded from http://proteininformatics.org/mkumar/bacarscan/
