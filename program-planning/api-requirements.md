


Agency staffer should be able to initiate the creation of a new endpoint by uploading a CSV or JSON file into an S3 bucket.  
The file upload should trigger the DB to ingest the data file.  
The API should then generate an endpoint at api.agency.gov/name_of_file that allows querying via parameter_1&parameter2, etc.  


...  

Overwriting a file should prompt a refresh of the API endpoint.  
Deleting a file should prompt the removal of the API endpoint.  

