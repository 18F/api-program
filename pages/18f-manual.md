---
layout: page
title:  "18F Manual"
permalink: /18f-manual/
---

_Below are directions for common tasks for the 18F team that is participating in an API Program engagement.  Further documentation will be regularly added, but you can also file requests for something specific in the [issue tracker](https://github.com/18F/api-program/issues)._

## Process for Onboarding a New Agency

### How to set up an agency with cloud.gov 

If an agency does not have a cloud.gov instance yet, go to #cloud-gov-business and request an agency sandbox be created and provide the email addresses as the user accounts that should be created.  Those people will receive emails when the account is created.  

_Note: You'll need to follow up and upgrade the cloud.gov instance to a FISMA Low isntance._

### How to gain access to the agency's cloud.gov instance.  

### How to set up autoapi in the agency's cloud.gov instance  New Instance of the API

* See instructions [here](https://github.com/18F/autoapi/blob/master/instructions.md). 

### How to Get DNS Access From the New Agency

...

### Request DNS set up for api.[agency].gov




### Set up api.data.gov for the autoapi instance

Once the autoapi instance has been stood up... 

* Log into api.data.gov/admin.  
* Configuration -> API Backends -> Add API Backends 
  * Backend Protocol: HTTPS
  * Server: Name of Backend Host 
  * Frontend Host: api.[agency].gov
  * Backend Host: [subdomain of hosted autoapi instance]
  * Matching URL Prefixes - Frontend Prefix: /data/
  * Matching URL Prefixes - Backend Prefix: /
  * Save
* Configuration -> Publish Changes (Check only your API)

_If the DNS delegation for api.[agency].gov is not yet compete, set up the API analytics at api.18f.gov/[agency] so that we can begin using the API._

### Set up access to api.data.gov analytics  

* Users -> API Scopes -> Add New API Scopes
  * Name: [Agency] - AutoAPI 
  * Host: api.[agency].gov
  * Path Prefix: /data/
  * Save
* Users -> Admin Groups -> Add New Admin Group
  * Group Name: [Agency] - AutoAPI 
  * Permissions: [all]
* Users -> Admin Accounts -> Add New Admin
  * Username: [their email address] 
  * Permissions - Groups: [Agency] - AutoAPI 



