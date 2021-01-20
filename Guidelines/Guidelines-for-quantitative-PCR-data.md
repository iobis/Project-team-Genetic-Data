### Occurrence core
&nbsp;  
Recommended DwC-A occurrence core fields from the [GBIF guidelines](https://docs.gbif-uat.org/publishing-dna-derived-data/1.0/en/). 
The occurrence core for ddPCR/qPCR data:  
&nbsp;

| Term   |     Example     |  Status |
|----------|-------------|------|
| BasisOfRecord |  MaterialSample | Required |
| occurrenceStatus |  Present, Absent | Required |
| eventDate | 2020-01-05 |   Required |
| [scientificName](#scientificName) |  Gadus morhua L. 1758 |    Required |
| eventID |       |   Highly recommended|
| recordedBy | "Jane Smith" |   Highly recommended | 
| organismQuantity | 50 |   Highly Recommended |
| organismQuantityType | dd/dPCR droplets |   Highly Recommended |
| [sampleSizeValue](#sampleSizeValue) | 20000 |   Highly Recommended|
| sampleSizeUnit | ddPCR droplets, qPCR number |   Highly Recommended |
| materialSampleID | e.g. biosample ID |   Highly Recommended |
| decimalLatitude | 60.545207 |   Highly Recommended |
| decimalLongitude | 24.174556 |   Highly Recommended |
| kingdom | Animalia |   Highly Recommended |
| phylum | Chordata |   Recommended|
| class| Actinopterygii |   Recommended|
| order | Gadiformes |   Recommended |
| family | Gadidae |   Recommended|
| genus | Gadus |   Recommended |


&nbsp;
### Extension for mapping metabarcoding data  
&nbsp;Recommended fields from the [DNA derived data extension](https://rs.gbif.org/sandbox/extension/dna_derived_data.xml) for ddPCR or qPCR data. This is the current recommendation from GBIF, but will be developed based on discussion with MixS standards  
&nbsp;   
 
| Term   |     Example     |  Status |
|----------|-------------|------|
| sop | protocol| Highly Recommended |
| annealingTemp | 60 | Highly Recommended |
| annealingTempUnit | Degree Celsius | Highly Recommended |
| [pcr_cond](#pcr_cond) | all conditions | Highly Recommended |
| probeReporter | FAM | Highly Recommended |
| probeQuencher | NFQ-MGB | Highly Recommended |
| ampliconSize | 83 | Highly Recommended |
| quantificationCycle | 0.3 | Highly Recommended for qPCR |
| baselineValue | 15 | Highly Recommended for qPCR |
| thresholdQuantificationCycle | 37.9450950622558 | |
| automaticThresholdQuantificationCycle | no | |
| automaticBaselineValue | no | |
| contaminationAssessment | no | |
| [estimatedNumberofCopies](#estimatedNumberofCopies) | 10300 | |
| amplificationReactionVolume | 22 | |
| amplificationReactionVolumeUnit | µl | |
| pcr_analysis_software | BIO-RAD QuantaSoft | |
| [experimentalVariance](#experimentalVariance) | | |
| target_gene| 16S, 18S, COI.. | Highly Recommended  |
| target_subfragment |  V3,V4,V6,V9,ITS    |   Highly recommended|
| pcr_primer_forward |  GGACTACHVGGGTWTCTAAT |   Highly recommended | 
| pcr_primer_reverse |  GGACTACHVGGGTWTCTAAT |   Highly Recommended |
| pcr_primer_name_forward | jgLCO1490 |   Highly Recommended |
| pcr_primer_name_reverse | jgHCO2198 |   Highly Recommended|
| pcr_primer_reference | doi |   Highly Recommended |
| env_broad_scale| forest biome [ENVO:01000174] |   Recommended |
| env_local_scale| litter layer [ENVO:01000338] |   Recommended |
| env_medium | soil[ENVO:00001998] |   Recommended |
| concentration | 67.5 |   Recommended |
| concentrationUnit | ng/µl |  Recommended |
| methodDeterminationConcentrationAndRatios | Nanodrop, Qubit | Recommended |
| ratioOfAbsorbance260_230 | 1.89 | Recommended |
| ratioOfAbsorbance260_280 | 1.91 | Recommended |
| samp_collect_device | biopsy, niskin bottle, push core | Recommended |
| samp_mat_process | filtering of seawater | Recommended |
| sampleVolume | 5 | Recommended |
| sampleVolumeUnit | liter | Recommended |
| size_frac | 0-0.22 µm | Recommended |
| pcr_primer_lod | 51 | Highly Recommended |
| pcr_primer_loq | 184 | Highly Recommended |

&nbsp;
&nbsp;
&nbsp;

### scientificName

Latin name of the closest known taxon (species or higher). GBIF accepts also an OTU identifier from BOLD or UNITE. At the moment OBIS is not yet connected to BOLD, but this is planned for the near future. It is recommended to use the highest taxonomy possible, and record the sequence for detailed classifications and searches.

### sampleSizeValue
In the case of dd/dPCR, the number of accepted partitions (n), e.g. meaning accepted droplets in ddPCR or chambers in dPCR.

### pcr_cond
	
Description of reaction conditions and components of PCR in the form of "initial denaturation:94degC_1.5min; annealing=…​"  	
Example:
initial denaturation:94_3;annealing:50_1;elongation:72_1.5;final elongation:72_10;35

### estimatedNumberofCopies

Number of target molecules per µl. Mean copies per partition (?) can be calculated using the number of partitions (n) and the estimated copy number in the total volume of all partitions (m) with a formula ?=m/n. Could this be in SampleSizeValue for qPCR?

### experimentalVariance

Multiple biological replicates are encouraged to assess total experimental variation. When single dPCR experiments are performed, a minimal estimate of variance due to counting error alone must be calculated from the binomial (or suitable equivalent) distribution.
