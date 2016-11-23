# Documentation
The documentation for the STAR program can be viewd at https://github.com/alexdobin/STAR/blob/master/doc/STARmanual.pdf. 

The documentation for the HTSeq program can be viewed at http://www-huber.embl.de/users/anders/HTSeq/doc/count.html.

# Before running star.sh
Download and store the GCRC_Session2-master.zip file in your $SCRATCH directory. Then make all bash scripts executable.

```bash
cd $SCRATCH
# Make STAR directory to store the results
mkdir STAR

# Unzip the GCRC_Session2-master.zip file and make bash scripts executable
unzip GCRC_Session2-master.zip
cd GCRC_Session2-master/scripts/
chmod a+x *.sh

```
# Run STAR index first with runSTARindex.sh
I added the runSTARindex.sh to run the STAR index once. You will need to make this file executable with chmod a+x command and then you could submit it as a qsub job as follows:

```bash
#!/bin/bash
#PBS -l nodes=1:m96G
#PBS -l walltime=47:58:00
#PBS -N **YourJobName**
#PBS -r n
#PBS -A **your-pi-ccri**

cd GCRC_Session2-master/scripts/
./runSTARindex.sh
```

# Before running qsub eg_star.pbs file
Please remember to modify the pbs files so that it matches your PI's CCRI id and modify the job name accordingly.
This is true for all .pbs files uploaded to this repository.

```bash
#!/bin/bash
#PBS -l nodes=1:m96G
#PBS -l walltime=47:58:00
#PBS -N **YourJobName**
#PBS -r n
#PBS -A **your-pi-ccri**
```
