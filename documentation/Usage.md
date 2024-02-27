# Basic Usage

Log into the development APIM instance and create or update a component:

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/b2c89072-9b78-4f0e-b568-e3697a6e4b51)

Once your changes have been made, navigate to the GitHub repository, click on 'Actions'. On the left hand side, select the 'Run - Extractor' option. This will extract the configuraton changes you've made in APIM into the a new auto-generated branch in the repository: 

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/73044c74-c05d-4847-ba60-a85bb302a2a2)


![image](https://github.com/alexmcdonald11/apiops/assets/141607968/34f854f3-b849-4126-9d3b-92e2720bf34b)

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/e0344849-47cd-48f1-911a-cbf04dd6267e)



The process will then automatically create a pull request for the new branch to be merged into the main branch:

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/6ce829ce-5515-4148-a5a8-e8c247a044cc)


Once the PR has been completed, the action workflow will deploy the artifacts into the development environment in order to test the new artifacts and ensure all deployed code is up to date. If this is successful, an approval will be requested in order to deploy the changes to prod:








# Environment-specific variables / configuration

