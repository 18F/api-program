---
layout: page
title:  "Agency API"
permalink: /agency-api/
---

The API itself is a simple, user-friendly API engine for an agency to use.  It resides at `https://api.[agency].gov/data/` and is managed by adding, overwriting, and deleting flat files in an Amazon S3 bucket.  

When a new file is uploaded into the bucket, an API is generated at `https://api.[agency].gov/data/name-of-file`.  Each column header in the flat file results in a query parameter for the API.   

#### Analytics 

The [api.data.gov service](https://api.data.gov/about) is invisibly integrated into the API to provide: 
* API keys, 
* Usage tiers, and 
* Robust analytics on who is using your API, how, and how much.

#### Other Details 

* The file size limit is _____.  
* You can host up to _______ files.   
* Supported file formats are: 'fixed', 'xls', 'xlsx', 'csv', 'json', 'geojson', 'ndjson`

