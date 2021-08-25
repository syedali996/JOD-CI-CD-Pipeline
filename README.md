This repository contains a github workflow that updates a published portal when a change is made to the API Specification in the master branch.

## Prerequisites
In order to use this workflow, you will require APIMatic Credentials with access to the APIMatic Api.  
This Api supports basic auth, if you would like to avoid storing your credentials in the workflow, you can use this [website](https://www.blitter.se/utils/basic-authentication-header-generator/) to encrypt them.  
Copy the encrypted key (the text that follows 'Authorization : Basic') and store it in a github secret called CREDENTIALS.  

You will also need to add the API Entity ID for the specific API version in the workflow. You can copy this from the APIMatic Dashboard and set the API_ENTITY_ID environment variable in the main.yml file.  

**Please note that the portal must be published manually at least once for this workflow to run successfully**
