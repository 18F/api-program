

# API Engine Requirements

## Characteristics 
* Agency should be able to run as many datasets through the API engine as desired (on the scale of 20-100 total).  
* It should be able to scale to very high use (~15 million API hits/month).  
* It should incorporate api.data.gov.  


## Workflows

1. Agency staffer should be able to initiate the creation of a new endpoint by uploading a CSV or JSON file into an S3 bucket.  
2. The file upload should trigger the DB to ingest the data file.  Or there should be a simple means of triggering the API engine to re-run (that does not involve the command line).  
3. The API should then generate an endpoint at api.agency.gov/name_of_file that allows querying via parameter_1&parameter2, etc.  


...  

Overwriting a file should prompt a refresh of the API endpoint.  
Deleting a file should prompt the removal of the API endpoint.  

