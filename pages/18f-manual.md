---
layout: page
title:  "18F Manual"
permalink: /18f-manual/
---

## Process for Onboarding a New Agency


### How to Set Up a New Instance of the API

... Deploy to Cloud.gov ...

### Set up Agency Access for the API and api.data.gov 

In the api.data.gov admin, complete the following steps to deploy the autoapi instance to `api.18f.gov/agency/`:

1. Create a new [API Scope](https://api.data.gov/admin/#/api_scopes) for `api.18f.gov/agency/`
2. Create a new [Admin Group](https://api.data.gov/admin/#/admin_groups) to give permissions to that API Scope.
3. Add any agency [Admin Accounts](https://api.data.gov/admin/#/admins) to that Admin Group.
4. Create and publish a new [API Backend](https://api.data.gov/admin/#/apis) pointing from `api.18f.gov/agency/` to wherever the underlying AutoAPI instance lives.

### How to Set Up the New Developer Hub

... 


### How to ATO the API and Developer Hub

... 

### How to Instantiate the API Program Artifacts

... 

## Process for Transitioning the API to the Agency's Ownership

1. After the agency [picks and assigns](/api-program/agency-manual/#how-to-set-up-the-api) their own domain to api.data.gov, repeat the [api.data.gov setup](#set-up-agency-access-for-the-api-and-apidatagov) for their own domain name.
2. ...
