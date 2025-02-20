# MyGenome Project

1. Retrieve sequence reads for project.
```bash
   scp bash
```
2. Initial count of total sequence reads in raw read data.
```bash
   example bash 
```
3. Assess sequence quality of raw read data using FASTQC.
```bash
   fastqc Pr88168_1.fq.gz Pr88168_2.fq.gz
```
Results:

![alt text](images/raw_forward_qual.png)

4. Retrieve adaptor file needed to trim adaptor content.
```bash
   scp for adaptors.fasta
```
5. Trim reads to address high adapter content using trimmomatic.
```bash
   trim bash
```
6. Assess sequence quality of the trimmed paired reads using FASTQC.
```bash
   fastqc Pr88168_paired_1.fq.gz Pr88168_paired_2.fq.gz
```
