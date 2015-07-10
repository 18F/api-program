

# API Engine Requirements

## Characteristics 
* Agency should be able to run as many datasets through the API engine as desired (on the scale of 20-100 total).  
* It should be able to scale to very high use (~15 million API hits/month).  
* It should incorporate api.data.gov.  


## Workflows

1. Agency should be able to initiate the creation of a new endpoint by uploading a CSV or JSON file into an S3 bucket.  
2. The file upload should trigger the DB to ingest the data file.  Or there should be a simple means of triggering the API engine to re-run (that does not involve the command line).  
3. The API should then generate an endpoint at api.agency.gov/name_of_file that allows querying via parameter_1&parameter2, etc.  
4. Overwriting a file should update the API.  
5. Deleting a file should remove the endpoint 

~~~~~~~~


* Easy to use
  * An 18F staffer should be able to train a non-technical agency staffer on how to add, edit, and remove data easily.
  * The agency staffer should be able to manage these tasks without the need for new software, since most government staff do not have admin permissions on their work computers.
* Easy for 18F to instantiate.
  * Minimal effort should be needed by 18F developers and devops to make ready new instances of it.
* Highly scalable.
  * There should be little or no limit to the number of datasets that can be added to the API. If an enthusiastic agency correctly integrates hundreds of simple data files, the API stack should not choke on the volume.
  * There should be little to no limit to the number of API hits that the API can handle. We should design the API so that it is simple yet robust. If an agency correctly published a dataset that for some reason became incredibly popular, the API should be able to scale to meet demand.
  * Cloud costs should scale linearly so that popularity and scalability are cheap.

