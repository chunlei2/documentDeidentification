This folder contains a sample of the data that will be released as a part 
of the two 2014 i2b2 challenge tracks. 

Each track has its own folder of sample data; the contents are outlined 
below.

----------------------------------------------

Track 1: De-identification 

Folder contents:

PHI/
	This folder contains only PHI-related annotations for the text 
in each document.  These files are the gold standard for the de-id track.

De-identification_guidelines_2014_distribution.pdf
	This file contains the guidelines for PHI identification

de-idi2b2_distribution.dtd
	This file is the DTD that describes the valid tags for the 
de-identification annotation task.

---------------------------------------------------

Track 2: Identifying risk factors for heart disease over time

Folder contents:

gold/
	This folder contains the gold standard annotations that will be used for
evaluation. These are document-level tags which are defined in the annotation
guidelines. Valid tags and attributes are outlined in the provided cardiac risk DTD

complete/
	This folder contains complete annotations for the entire text. It contains 
document level annotations. Each document level annotation is supplemented with tags 
that show the the evidence found by our annotators for a particular document level 
tag. These annotator tags include position information and are included with the hope 
that they will ease system development and error analysis.

i2b2_2014_annotation_guidelines_distribution.pdf
	This file contains the guidelines for the risk factor annotation 

cardiacRisk_distribution.dtd
	This file is the DTD that describes the valid tags for the 
risk factor annotation task

---------------------------------------------------

Overview of the sample files:

The gold/, complete/, and PHI/ folders each contain 8 XML files. These
files contain four discharge summaries each for two different patients. The file
names follow a consistent pattern with the first set of digits identifying the
patient and the last set of digits identifying the sequential record number

ie: XXX-YY.xml  
where XXX is the patient number,  and YY is the record number.

Example: 320-03.xml
This is the third (03) record for patient 320

Each file has a root level xml node <CardicaRiskTask> which will contain a
<TEXT> node that holds the medical annotation text and a <TAGS> node containing
annotations for the document text.  The specific annotations contained in each file 
are described by the accompanying DTDs and annotation guidelines.

---------------------------------------------------

