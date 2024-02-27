# Basic Usage

Log into the development APIM instance and create or update a component:

Once your changes have been made, navigate to the GitHub repository, click on 'Actions'. On the left hand side, select the 'Run - Extractor' option. This will extract the configuraton changes you've made in APIM into the a new auto-generated branch in the repository: 

The process will then automatically create a pull request for the new branch to be merged into the main branch:

Once the PR has been completed, the action workflow will deploy the artifacts into the development environment in order to test the new artifacts and ensure all deployed code is up to date. If this is successful, an approval will be requested in order to deploy the changes to prod:








# Environment-specific variables / configuration

