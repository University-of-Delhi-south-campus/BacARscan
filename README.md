# BacARscan: a Hidden Markov model based framework to discern diversity of antibiotic resistance genes in –omics datasets

BacARscan that can detect, predict and characterize ARGs in functional metagenomics data, including short sequencing reads and fragmented contigs. It is anticipated that this ability of BacARscan would be helpful in rapid monitoring, characterization and surveillance of ARG repertoire in bacterial communities at an early stage of infection/outbreak. We also expect that BacARscan would be helpful to the scientific community for quick monitoring of ARGs in a microbial population. 

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
