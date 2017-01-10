# UPDATES - 01/10/2017
Before running STAR also make sure you have an hg19.fa file present in $SCRATCH/Homo_sapiens/UCSC/hg19/Sequence/Chromosomes/. If you do not havd the hg19.fa file already, you can create one as follows:
```bash
cd $SCRATCH/Homo_sapiens/UCSC/hg19/Sequence/Chromosomes/
cat chr1.fa chr2.fa chr3.fa chr4.fa chr5.fa chr6.fa chr7.fa chr8.fa chr9.fa chr10.fa chr11.fa chr12.fa chr13.fa chr14.fa chr15.fa chr16.fa chr17.fa chr18.fa chr19.fa chr20.fa chr21.fa chr22.fa chrX.fa chrY.fa > hg19.fa
# Check that you have successfully created the hg19.fa file with the la command:
ls
```

# UPDATES - 11/23/2016
### STAR.sh file Updated ###
### Added runSTARindex.sh script to run STAR index separately ###

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
Or you can run it as a bash script on the cluster (getExampleFastq.sh script from this repository).

```bash
chmod a+x getExampleFastq.sh
./getExampleFastq.sh
# The files should start downloading in your $SCRATCH drive
```
# Before running .pbs files
Please remember to modify **abc-123-aa** with your PI's CCRI
```bash
#!/bin/bash
#PBS -A **abc-123-aa** 
#PBS -l walltime=30:00:00
#PBS -l nodes=2:ppn=8
#PBS -N runExample01
#PBS -r n
```
For more information on how to submit jobs on the Calcul Quebec clusters see https://wiki.calculquebec.ca/w/Exécuter_une_tâche/en#tab=tab1.

# Downloading files directly 
Alternatively, you can download the files from the links directly and transfer the files to your $SCRATCH drive on the cluster with FileZila. 

<sub>https://dl.dropboxusercontent.com/u/30969719/SRR1777876_accepted_hits_R1.fq.gz
https://dl.dropboxusercontent.com/u/30969719/SRR1777876_accepted_hits_R2.fq.gz
https://dl.dropboxusercontent.com/u/30969719/SRR1777877_accepted_hits_R1.fq.gz
https://dl.dropboxusercontent.com/u/30969719/SRR1777877_accepted_hits_R2.fq.gz</sub>

# Downloading the hg19 reference genome from Illumina's iGenomes
You will also need to download the hg19 reference genome from Illumina iGenomes at http://support.illumina.com/sequencing/sequencing_software/igenome.html. 
You can directly download and untar these files in your $SCRATCH drive as follows:

```bash
cd $SCRATCH
wget ftp://igenome:G3nom3s4u@ussd-ftp.illumina.com/Homo_sapiens/UCSC/hg19/Homo_sapiens_UCSC_hg19.tar.gz
tar -xzvf Homo_sapiens_UCSC_hg19.tar.gz
```

