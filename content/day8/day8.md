# sequences databases and file formats
## content to cover
- FASTQ files (format for NGS)
- QC reads before assebly process
- Reference based Genome assembly (steps)
- sequencing data and assembly file formats
- other file formats : alignment , profiles

## FASTA file format


## FASTQ file format
- contains quality with sequence
- contains four lines information
  1. `line 1` - identifier line contain unique identifier for the sequence , also contain some additional info.
       example:-
      * `EAS***` - unique instrument name
      * `136` - the run id
      * `FC70***` - flowcell id
      * `2` - flowcell lane
      * `2104` - no within the flowcell lane
      * `15343` - X coordinate
      * `197393` - Y coordinate
      * `1` - paired-end or mate-pair reads onlytext
      * `Y` - Y when read is filtered (bad quality reads), else N (good quality reads)
      * `18` - even no , 0 when non of the control bits are on
      * `ATCGCC` - index sequence
  2. `line 2` - actual sequence
  3. `line 3` - separator line generally mimics the line 1
  4. `line 4` - phred scores of each bases of sequence given in the line2

## FASTQC tools
- java based tools to generate the QC reports
- primer and adaptor to be removed using `trimmomatic`
- check quality control on raw sequence from high throughput pipelines
- after quality check if data has any problems then it goes to trimmomatic
- data might have 2 types of problems
  *  quality - we cut the sequence and take only the  part of the sequence for good quality
  *  techinal sequence or adaptors - during library preparation we add adaptors for reads to be run on the flowcell we use some adaptors to bind it with flowcell ( because flowcell has complementery seq)
- FASTQC check the primers and adaptors details
- then using trimmomatic we cut it out

## Reference based genome assembly and variant calling
![Screenshot](flowchart.jpg)

1. **align** - `BWA` or `bowtie`  align `Reference sequence` to  `NGS reads` and gives a SAM format file (sequence alignment map) and gives the SAM file
```bash
bwa mem reference.fasta reads.fastq > output.sam
```
2. **conversion** -  .then this `SAM` format is converted into `BAM` for computer understandable language. 
```bash
samtools view -S -b output.sam > output.bam
```
3. **sorting** - BAM file is sorted into `sorted BAM` by rearranging the reads according to the reference genome.
```bash
samtools sort output.bam -o sorted.bam
```
4. **indexing** -
5. **summarize** - usign `mpileup` commmand of the sam tools for base call (assingment identity) at each position , pileup data creates `RAW .bcf` file 
6.**view** - view from the bcftools convert the .bcf into .vcf file , listing all the variants(SNPs) .hence we get the VCF ( a tab seperated file - tell position of chromosome where is the SNP present )
7. **filtering**- filtering low-quality or non-significant variants using BEDtools provides Final VCF file
