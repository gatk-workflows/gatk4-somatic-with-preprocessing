# gatk-somatic-with-preprocessing

germline_single_sample_workflow :
This WDL pipeline implements data pre-processing and initial calling for somatic SNP,
Indel, and copy number variants in human whole-genome sequencing (WGS) data.

#### Requirements/expectations
 - Human whole-genome pair-end sequencing data in unmapped BAM (uBAM) format
 - One or more read groups, one per uBAM file, all belonging to a single sample (SM)
 - Input uBAM files must additionally comply with the following requirements:
 - - filenames all have the same suffix (we use ".unmapped.bam")
 - - files must pass validation by ValidateSamFile
 - - reads are provided in query-sorted order
 - - all reads must have an RG tag
 - Reference genome must be Hg38 with ALT contigs

 Runtime parameters are optimized for Broad's Google Cloud Platform implementation.
 For program versions, see docker containers.

### Software version requirements :
Cromwell version support 
- Successfully tested on v30.2
- Does not work on versions < v23 due to output syntax

### LICENSING :
 This script is released under the WDL source code license (BSD-3) (see LICENSE in
 https://github.com/broadinstitute/wdl). Note however that the programs it calls may
 be subject to different licenses. Users are responsible for checking that they are
 authorized to run all programs before running this script. Please see the docker
 page at https://hub.docker.com/r/broadinstitute/genomes-in-the-cloud/ for detailed
 licensing information pertaining to the included programs.
