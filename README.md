This repository contains a github workflow that updates a published portal when a change is made to the API Specification in the master branch.

## Prerequisites
In order to use this workflow, you will require an APIMatic account with access to the APIMatic Api.   
This Api supports Basic Auth as well as Auth Keys, you can learn how to generate an Auth Key [here](https://docs.apimatic.io/manage-apis/get-api-keys/). This tutorial uses an Auth Key stored in a github secret called CREDENTIALS. 

You will also need to add the API Entity ID for the specific API version in the workflow. You can copy this from the APIMatic Dashboard and set the API_ENTITY_ID environment variable in the main.yml file.  

**Please note that the portal must be published manually at least once for this workflow to run successfully**
