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

4. Retrieve adpators.fasta file needed to trim adapater content.
```bash
   scp for adaptors
```
5. Trim reads to address high adapter content using trimmomatic.
```bash
   trim bash
```
6. Assess sequence quality of the trimmed paired reads using FASTQC.
```bash
   fastqc Pr88168_paired_1.fq.gz Pr88168_paired_2.fq.gz
```
