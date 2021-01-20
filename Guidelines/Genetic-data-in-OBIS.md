One of the main discussion points of this working group is how genetic data will be dealt with in OBIS.
OBIS has the goal to develop:


**1. Sequence look-up service**
> Should be possible as long as the sequences are recorded. Will need to develop a sequence search algorithm (possibly something like the [DNA barcode browser](https://dna-barcode-browser.herokuapp.com/) developed by [Rod Page](https://iphylo.blogspot.com/) for GBIF.

**2. Update taxonomic assignments of sequences regularly**
>This will require a lot of computational power. Is it possible to do this by having direct links to BOLD binIDs for example?

**3. Reading data from the biom -format to DwC-A to make submission of data as simple as possible**
>This means developing a tool for the purpose

Other issues that will need to be discussed is **if** and how OBIS will deal with raw sequence data. A full data analysis pipeline will be developed for the [PacMAN](https://pacman.obis.org/) project, which could act as a use case, or as a full pipeline for other projects as well. 