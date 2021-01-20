Collecting, analysing and interpreting genetic  data can differ fundamentally from the traditional methods utilized in biodiversity research. In this section we discuss the different types of studies and the steps included in the workflow of genetic data collection. Due to the highly technical nature of environmental DNA analyses, there are many factors which may introduce biases into the data. To keep sequence derived occurrence data fully comparable it would be advisable to keep as much information as possible from each of these factors with the datasets added to OBIS.

## Data types  
Most of the time, the sequence is not linked to an archived specimen, but is derived from mixed environmental samples. In this case, genetic data represents a molecular trace of the organisms found in the environment, and therefore a lot of care needs to be taken when interpreting results of environmental DNA (eDNA) surveys. The different analysis types that result in sequence data are:

#### 1. Sequences linked to specimens  
This is the most similar case to traditional biodiversity data and results in reliable data that supports other studies. Online databases that record and give indicators for specimen linked genetic data exist for specific marker genes. For example BOLD for the cytochrome oxidase gene I (COI) and UNITE for ITS. 

#### 2. Biomarkers sequenced from environmental samples
One of the most commonly analysed sample types that result in large amounts of sequence information. Biomarkers are short gene sequences that are targeted and used to identify the taxonomy of organisms. Most commonly used biomarkers in biodiversity research are variable regions of the 18S/16S/12S rRNA gene, COI gene or ITS.

#### 3. Metagenomes
Metagenomics describes the sequencing of all DNA found in a sample without targeting and amplifying specific regions in the genomes. Due to the addition of functional genetic information as well as avoiding biases arising from amplification of DNA, this method is gaining traction in studies in microbiology. It is also possible to derive occurrence data from metagenomics information. Biomarker fragments can be searched from the genetic information using bioinformatics, or comparisons of taxonomy can be made utilizing information from a collection of genetic sequences (commonly compared in studies in microbiology).

#### 4. Quantitative PCR analysis
Quantitative PCR can be used to identify and quantify the amount of a specific target sequence in the environmental sample. In this case the target sequence is known beforehand, and only the presence (abundance) or absence of one sequence is recorded. 

## Sampling workflow

#### Sampling specimen/environmental substrate
The choice of sampling method will effect the sequences recorded greatly. Whatever the sampling choice, it is impossible to get a fully representative sample of the target environment. Therefore comparison of absences or abundances of specific sequences from a sample is difficult, unless the samples have been collected in a comparable manner. For example the choice of filter pore size when collecting water samples will result in a completely different distribution of sequence information.

#### DNA Amplification
After DNA extraction is where the workflow changes depending on the type of study. For metagenomics sequence library preparation will be directly from the extracted DNA. For qPCR the presence of the specific target gene will likewise be analysed from the extracted DNA. However, for the analysis of marker gene diversity in the sample the next required step will be DNA amplification. This will most likely be the most commonly used method in biodiversity studies.

The results will depend mainly on the chosen primers that are used in the study. To a lesser extent the results can be influenced by the number of amplification cycles used in the amplification step. Several studies will also record occurrences with multiple primer sets, that is multiple biomarkers.  

#### Sequencing
The chosen sequencing platform and parameters will define how deeply the samples are sequenced. For example the detection of rare or low-abundance organisms may require a different approach than the detection of common organisms. However for the presence of specific biomarkers, the chosen sequencing method should have minimum effect compared to all other factors in the sampling workflow. 

#### Sequence analysis
A major step in the workflow for obtaining sequence derived occurrence data is the bioinformatic analysis of raw sequences. This includes quality control steps, clustering by the actual sequence (OTUs or ASVs) searching for sequencing errors and filtering out low abundance sequences (indistinguishable from errors). The final product is a sequence by sample table that records the abundance of each sequence. Sequence data is always compositional, meaning that it represents the relative abundance of each sequence in the sample and is not related to its actual abundance in the environment. There are no standard workflows in use at the moment, and therefore the method of analysis needs to be well documented. Alternatively OBIS could run a standard workflow on raw sequences.  

#### Taxonomic analysis of sequences
The taxonomic databases and algorithms used to classify sequences under different scientific names is the most important step in terms of sequence occurrence data. Databases with verified taxonomies are not complete, and misclassifying sequences is relatively common. Often, the taxonomic annotation of sequences can also be ambiguous, specifically in the case of 18S rRNA gene, the taxonomic resolution is generally not enough to record species-level occurrences. It is possible to accept this and record only the highest available taxonomic rank. However, there is also value in being able to search the occurrences of specific sequences whose exact classification remains unknown. Therefore we suggest that OBIS devise a system where it is possible to search based on sequences. Thereafter it should be discussed in the case of sequence information, if it should not always be required to provide the scientific name linked to it, but that this information is kept in a separate table linking sequences with the best available current information by OBIS. 

According to current practices, raw sequence information is generally already submitted to public sequence databases. In terms of recording occurrences to be able to compare them across studies like in the case of OBIS, many of the issues remaining in the interpretation of genetic data can be mitigated by keeping a continuous link to the raw sequence information. If OBIS can act as a workflow analysing and packaging data submitted to public databases, it could keep a highly comparable and updatable database of sequence derived occurrences. 






