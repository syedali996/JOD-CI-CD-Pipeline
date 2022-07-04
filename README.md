This repository demonstrates how APIMatic's API can be used to keep API Documentation and SDKs updated via CI/CD.

The [_main.yml_](https://github.com/apimatic/hosted-portal-workflow/blob/master/.github/workflows/main.yml) file contains a github workflow that updates the APIMatic portal when the respective API Specification is modified.


## Prerequisites
 [Generate an API KEY](https://docs.apimatic.io/account-management/obtaining-auth-keys/) before proceeding.   
    
    
   
## Try it out
Follow these steps to try out this workflow for yourself:


1. Import an API into your APIMatic account.
2. Get the API Entity ID for this newly imported API as described in [APIMatic's documentation.](https://docs.apimatic.io/manage-apis/get-api-keys/)
4. Fork this repository.
5. Create 2 new Github repository secrets in the forked repository:
    - API_KEY to store your APIMatic API Key
    - API_ENTITY_ID to store the API Entity ID you generated in step 2.     
6. Modify the API Specification stored in your repository and push your changes to the 'master' branch. This should trigger the CI/CD workflow. You can also manually trigger it via the 'Actions' tab in your repository.
3. [Generate a portal](https://docs.apimatic.io/getting-started/creating-your-first-portal/) for the API that you imported in step 1 and preview the API Docs.
7. The generated Portal should contain the changes you made to the API Specification.

**The steps above do not include Portal publishing. If you want to automate the publishing step as well, uncomment the last workflow step in the _main.yml_ file. 
However, please note that the portal must be [published](https://docs.apimatic.io/publish-apis/hosting-your-portal/) manually at least once for the publish step in this workflow to run successfully.
