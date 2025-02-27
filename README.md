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
<h2>Quality score for raw forward and reverse reads.</h2>
<p float="middle" style = "inline-block">
   <img src="images/raw_forward_qual.png" width="450" height="350">
   <img src="images/raw_reverse_qual.png" width="450" height="350">
</p>
<h2>Adaptor content for raw forward and reverse reads.</h2>
<p float="middle">
   <img src="images/raw_foward_adapt.png" width="450" height="350">
   <img src="images/raw_reverse_adapt.png" width="450" height="350">
</p>

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
