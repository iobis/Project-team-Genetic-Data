### Occurrence core
&nbsp;  
Recommended DwC-A occurrence core fields from the [GBIF guidelines](https://docs.gbif-uat.org/publishing-dna-derived-data/1.0/en/). 
The occurrence core for metabarcoding data:  
&nbsp;

| Term   |     Example     |  Status |
|----------|-------------|------|
| BasisOfRecord |  MaterialSample | Required |
| eventDate | 2020-01-05 |   Required |
| [scientificName](#scientificName) |  Gadus morhua L. 1758 |    Required |
| [scientificNameID](#scientificNameID) | urn:lsid:marinespecies.org:taxname:126436 | Required |
| occurrenceStatus | present | Required |
| eventID |       |   Highly recommended|
| recordedBy | "Jane Smith" |   Highly recommended | 
| organismQuantity | 33 |   Highly Recommended |
| organismQuantityType | DNA sequence reads |   Highly Recommended |
| sampleSizeValue | 1233890 |   Highly Recommended|
| sampleSizeUnit | DNA sequence reads |   Highly Recommended |
| materialSampleID | e.g. biosample ID |   Highly Recommended |
| decimalLatitude | 60.545207 |   Highly Recommended |
| decimalLongitude | 24.174556 |   Highly Recommended |
| [taxonID](#taxonID) | MD5 hash or OTU ID |   Highly Recommended (if no DNA sequence)|
| kingdom | Animalia |   Highly Recommended |
| phylum | Chordata |   Recommended|
| class| Actinopterygii |   Recommended|
| order | Gadiformes |   Recommended |
| family | Gadidae |   Recommended|
| genus | Gadus |   Recommended |
| [associatedSequences](#associatedSequences) | raw sequence reads |   Recommended |
| [identificationRemarks](#identificationRemarks) |annotation confidence |   Recommended |
| [identificationReferences](#identificationReferences) |bioinformatics pipeline|   Recommended |
| samplingProtocol |  |    |

&nbsp;
### Extension for mapping metabarcoding data  
&nbsp;Recommended fields from the [DNA derived data extension](https://rs.gbif.org/sandbox/extension/dna_derived_data.xml) for metabarcoding data. This is the current recommendation from GBIF, but will be developed based on discussion with MixS standards  
&nbsp;   
 
| Term   |     Example     |  Status |
|----------|-------------|------|
| DNA_sequence |  ACTG... | Highly Recommended |
| sop | protocol| Recommended |
| target_gene| 16S rRNA, 18S rRNA, nif, amoA, rpo, co1 | Highly Recommended  |
| target_subfragment |  V3,V4,V6,V9,ITS    |   Highly recommended|
| pcr_primer_forward |  GGACTACHVGGGTWTCTAAT |   Highly recommended | 
| pcr_primer_reverse |  GGACTACHVGGGTWTCTAAT |   Highly Recommended |
| pcr_primer_name_forward | jgLCO1490 |   Highly Recommended |
| pcr_primer_name_reverse | jgHCO2198 |   Highly Recommended|
| pcr_primer_reference | doi |   Highly Recommended |
| env_broad_scale| forest biome [ENVO:01000174] |   Recommended |
| env_local_scale| litter layer [ENVO:01000338] |   Recommended |
| env_medium | soil[ENVO:00001998] |   Recommended |
| lib_layout | Paired |   Recommended |
| seq_meth | Illumina HiSeq 1500 |   Highly Recommended|
| votu_class_appr | cutoffs for classifying|   Highly Recommended |
| votu_seq_comp_appr | "blastn;2.6.0+;e-value cutoff: 0.001" |   Highly Recommended |
| votu_db| "UNITE;8.2" |  Highly Recommended |

&nbsp;
&nbsp;
&nbsp;

### scientificName

Latin name of the closest known taxon (species or higher). GBIF accepts also an OTU identifier from BOLD or UNITE. At the moment OBIS is not yet connected to BOLD, but this could be planned. It is recommended to use the highest taxonomy possible, and record the sequence for detailed classifications and searches.

### scientificNameID
If no taxonomic ranks (no kingdom) are available, and therefore no ID's possible, it is possible for now to add the id for 'biota'. We are not sure yet how this will work with GBIF.

### taxonID
For eDNA data, it is recommended to use an MD5 hash of the sequence and prepend it with “ASV:”. Here the OTU id of different reference databases can also be recorded. For example BOLD bin ids, or genbank ids. 

### associatedSequences

A list (concatenated and separated) of identifiers (publication, global unique identifier, URI) of genetic sequence information associated with the Occurrence. Could be used for linking to archived raw barcode reads and/or associated genome sequences, e.g. in a public repository. Can be the same as materialSampleID.

### identificationRemarks

Specification of taxonomic identification process, ideally including data on applied algorithm and reference database, as well as on level of confidence in the resulting identification. Example: RDP annotation confidence (at lowest specified taxon): 0.96, against reference database: GTDB.

### identificationReferences

Link to the used bioinformatics pipeline 	

https://www.ebi.ac.uk/metagenomics/pipelines/4.1  
https://github.com/terrimporter/CO1Classifier
	


