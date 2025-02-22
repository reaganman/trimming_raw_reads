# Trimming Raw Reads Worksheet

<!--- Write name below --->
## Name: Reagan McKee

<!--- For this worksheet, answer the following questions--->

## Q1: What does "cleaning" your reads mean?
Answer: Removeing position and reads with low quality and removing the adapter sequences

### Q2: Open the script called "trim_raw_reads.sh". For every line that says ```insert description here```, replace that text with a description of what the line will do

### Q4: Attach an image of the plot from fastqc showing the average base quality from your reads files
![before-trimming-PHRED-plot-1](./images/read1_average_base_quality.png)
![before-trimming-PHRED-plot-1](./images/read2_average_base_quality.png)

---

## The following questions pertain to your first fastp run (without altering the parameters)
### Q5: How many reads were there in the R1 file before filtering?
Answer: 33967298
### Q6: How many bases were there in the R1 file before filtering?
Answer: 3430697098
### Q7: What proportion of bases were above PHRED score of 20 before filtering?
Answer: 95%
### Q8: What proportion of bases were above PHRED score of 30 before filtering?
Answer: 92%

### Q13: How many reads were there in the R2 file before filtering?
Answer: 33967298 sequences
### Q14: How many bases were there in the R2 file before filtering?
Answer: 3430697098
### Q15: What proportion of bases were above PHRED score of 20 before filtering?
Answer: 95
### Q16: What proportion of bases were above PHRED score of 30 before filtering?
Answer: 90

### Q17: How many reads were there in the merged file after filtering?
Answer: 12295196
### Q18: How many bases were there in the merged file after filtering?
Answer: 1750796378
### Q19: What proportion of bases in the merged file were above PHRED score of 20 after filtering?
Answer: 99
### Q20: What proportion of bases in the merged file were above PHRED score of 30 after filtering?
Answer: 95

### Q21: What is the difference between the merged and unmerged files (in principle, not quantitatively)?
Answer: unmerged files represent the seperate reads sequenced from forward and reverse strands in paired end sewuencing
### Q22: Why are the unmerged files for R1 and R2 different lengths?
Answer: The quality scores were not the same so reads were not filtered evenly

---

## The following questions pertain to Remix 1 (the first time you change fastp parameters)
### Q23: What parameters did you change?
Answer: -M from 20 to 25
### Q24: How did you expect this to change the filtering results (be specific)?
Answer: Not very much because most of the bases already had a phred score > 20. Other than that ther might be a slight decrease in the number of merged reads. 
### Q25: Explain the results. Did the change cause an effect that matched your expectations? Use information from the fastp output to explain.
Answer: 12198733 meged and filterd reads in remix1 compared to 12295196 originally so there were 96463 new reads filtered
THis makes since since before reads with a mimum average score of 20 would be merged.

---

## The following questions pertain to Remix 2 (the second time you change fastp parameters)
### Q26: What parameters did you change?
Answer: -l from 15 to 10
### Q27: How did you expect this to change the filtering results (be specific)?
Answer: There might be more reads merged because the size total size after filtering could be less
### Q28: Explain the results. Did the change cause an effect that matched your expectations? Use information from the fastp output to explain.
Answer: There were 12305164 merged and filtered reads in remix2, mean that 9968 more reads were merged after filtering, matching expectations.

