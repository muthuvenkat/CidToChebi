# CidToChebi  

CidToChebi is a Knime Workflow that creates a SDF file by fetching information from PubChem for Structure, Name & Biological Description (IUPAC Condensed and IUPAC). It also looks at glycan resource called GlyTouCan to retrieve the WURCS information. 

The pipeline contains two subpipelines first one to create the SDF from PubChem & GlyTouCan, second one classifies the compounds using Classyfire and prepares the SDF as headers required to be loaded into ChEBI Bulk Submission.

# Input 
A CSV file with the headers "GLYTOUCAN_ACC,PUBCHEM_CID" and please make sure input CID from pubchem should be just numbers as "70678538" not as "CID70678538". These two are requirements for the pipeline, hopefully if the pipeline doesnt run these two should be the main culprits rest shouldn't be an issue.

# Warning 
After Classification of entries, please check whether all the entries are classfied, in some cases ClassyFire fails to classify the entries resulting in missing entries after classification. 
