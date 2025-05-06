# MyGenome Project

Will go through and fix steps with actual code

1. Retrieve sequence reads for project.
```bash
   scp ngs lab 
```
## First I needed to assess the quality and trim of the sequence data I was working with

1. Initial count of the total number of sequence reads in the raw read data
```bash
   awk 'NR % 4 == 2 {s++} END {print s}' Pr88168_1.fq
```
This gave me a total of 9,078,004 raw reads (single end)

2. Assess sequence quality of raw read data using FASTQC.
```bash
   fastqc Pr88168_1.fq.gz Pr88168_2.fq.gz
```
<h2>Quality score for raw forward and reverse reads.</h2>
<p float="middle">
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

7. Transfer trimmed Pr88168 paired reads to MCC.
```bash
   scp jrhu252@jrhu252.cs.uky.edu:MyGenome/Pr88168_paired_1.fq.gz .(MCC/jrhu252 Directory)
   scp jrhu252@jrhu252.cs.uky.edu:MyGenome/Pr88168_paired_2.fq.gz .(MCC/jrhu252 Directory)
```

