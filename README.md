# GCRC_Session2
Source code and files required for the GCRC bioinformatics workshop - Session 2 are available in this repository.

Windows Users:
Please download Putty available at http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html.

Mac & Windows Users:
To transfer files between the cluster and computer, please download Filezilla available at https://filezilla-project.org/download.php?show_all=1. 

# Files required for the workshop
Please download this repository and download the files required for the workshop before attending the class. It may take 1-2 days to download everything depending on your internet connection. To save time, I suggest you download everything directly to your $SCRATCH drive on the cluster. 

You can download the RNA seq fastq files used in the examples directly into your $SCRATCH drive on the cluster, as follows:
Login to cluster, then in the terminal enter:

```bash
cd $SCRATCH
wget https://dl.dropboxusercontent.com/u/30969719/SRR1777876_accepted_hits_R1.fq.gz
wget https://dl.dropboxusercontent.com/u/30969719/SRR1777876_accepted_hits_R2.fq.gz 
wget https://dl.dropboxusercontent.com/u/30969719/SRR1777877_accepted_hits_R1.fq.gz
wget https://dl.dropboxusercontent.com/u/30969719/SRR1777877_accepted_hits_R2.fq.gz
```
Or you can launch it as a job on the cluster (download pbs script from this repository).

```bash
qsub getExampleFastq.pbs
```

Alternatively, you can download the files from the links directly and transfer the files to your $SCRATCH drive on the cluster with FileZila. 

<sub>https://dl.dropboxusercontent.com/u/30969719/SRR1777876_accepted_hits_R1.fq.gz
https://dl.dropboxusercontent.com/u/30969719/SRR1777876_accepted_hits_R2.fq.gz
https://dl.dropboxusercontent.com/u/30969719/SRR1777877_accepted_hits_R1.fq.gz
https://dl.dropboxusercontent.com/u/30969719/SRR1777877_accepted_hits_R2.fq.gz</sub>

You will also need to download the hg19 and mm10 reference genome from Illumina iGenomes at http://support.illumina.com/sequencing/sequencing_software/igenome.html. 
You can directly download and untar these files in your $SCRATCH drive as follows:

```bash
cd $SCRATCH
wget ftp://igenome:G3nom3s4u@ussd-ftp.illumina.com/Homo_sapiens/UCSC/hg19/Homo_sapiens_UCSC_hg19.tar.gz
tar -xzvf Homo_sapiens_UCSC_hg19.tar.gz
```

