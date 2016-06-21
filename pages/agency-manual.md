---
layout: page
title:  "Agency Manual"
permalink: /agency-manual/
---

_Below are directions for common tasks for the core team at the agency client.  Further documentation will be regularly added, but you can also file requests for something specific in the [issue tracker](https://github.com/18F/api-program/issues)._   
  
## Setting up the API

### Creating a cloud.gov account

https://docs.cloud.gov/intro/overview/using-cloudgov-paas/

### Granting 18F access to your cloud.gov sandbox 

1. Log into console.cloud.gov
2. In the top left, choose `Change Organization -> SANDBOX`.  
3. Click on your name (first.last). 
4. Click on the `User Management` tab.  
5. Click on the `All SANDBOX Org Users` tab.  
6. Search for the 18F staff who are requesting access and click on their name.  
7. Switch all three permissions (`Space Manager`, `Space Developer`, and `Space Auditor`) from `Off` to `On`.  

## Using the API 

### Accessing the S3 bucket 

With this API engine, you will add, update, or remove APIs is by uploading, overwriting, or deleting static files in the specific S3 bucket.  There are [many ways of interacting with S3 buckets](https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=how%20to%20access%20s3%20bucket). For instance, [Cyberduck](https://cyberduck.io/?l=en) is a free, open source tool that works on Windows and Mac computers.  

Regardless of which tool you use, you will need the following information:  

* access_key_id (may also be labeled 'username')
* bucket (may also be labeled 'path')
* secret_access_key (may also be labeled 'password')

Once you have authenticated to your S3 bucket, you will be able to do the following.  

### How to add a dataset 

* Prepare a machine-readable data file on your computer. 
* Depending on the S3 client you are using, there may be several ways to upload files, but many will have an upload button or allow you to drag and drop the static file into the client window.  
* Note that formatting errors in the data file may keep the API from generating.  If the dataset was successfully uploaded and the automated API documentation is not updated within 30 seconds, there was likely a formatting issue with the data file.  You will need to review the static data file, normalize it, and re-upload it in order to successfully generate the API. 
* The API will be accessible at [api-base-url/name-of-file-that-was-uploaded].  

### How to edit a dataset 

* In order to update an existing API, prepare a machine-readable data file on your computer that has the same file name that was uploaded originally. 
* Follow the same steps of adding a dataset but when prompted, choose to overwrite the file in the S3 bucket.  
* Note that formatting errors in the data file may keep the API from updating.  If the dataset was successfully uploaded and the automated API documentation is not updated within 30 seconds, there was likely a formatting issue with the data file.  You will need to review the static data file, normalize it, and re-upload it in order to successfully generate the API. 
* The API will be accessible at the same URL - [api-base-url/name-of-file-that-was-uploaded].  


### How to remove a dataset

* Using your S3 client, delete the static file.  

### How to view the API analytics 

* Log in at api.data.gov/admin.  
* To see how the API is being used, navigate to Analytics -> API Drilldown.  
* API hits can be individual examined or measured via a wide range of queries at Analytics -> Filter Logs.  
* API activity can be viewed specific to each developer key in order to analyze who is using the API and how much and how their application is being used.  This can be found at Analytics -> By Users.  

