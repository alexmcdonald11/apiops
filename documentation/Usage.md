# Basic Usage

Log into the development APIM instance and create or update a component:

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/b2c89072-9b78-4f0e-b568-e3697a6e4b51)

Once your changes have been made, navigate to the GitHub repository, click on 'Actions'. On the left hand side, select the 'Run - Extractor' option. This will extract the configuraton changes you've made in APIM into the a new auto-generated branch in the repository: 

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/a5ca4207-a766-4f4f-a047-5577258323bf)


![image](https://github.com/alexmcdonald11/apiops/assets/141607968/34f854f3-b849-4126-9d3b-92e2720bf34b)

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/e0344849-47cd-48f1-911a-cbf04dd6267e)



The process will then automatically create a pull request for the new branch to be merged into the main branch:

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/6ce829ce-5515-4148-a5a8-e8c247a044cc)


Once the PR has been completed, the action workflow will deploy the artifacts into the development environment in order to test the new artifacts and ensure all deployed code is up to date. If this is successful, an approval will be requested in order to deploy the changes to prod:

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/c5bb55ce-9957-41ef-b4b9-6cd988182b9f)

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/0d89552f-0e79-4fd9-a40e-a270e22cbc93)

![image](https://github.com/alexmcdonald11/apiops/assets/141607968/5c3dc0d3-df6b-4958-a11b-b3eafa3886f2)





# Environment-specific variables / configuration

When deploying APIM artifacts across environments, it's common to maintain a set of environment-specific values. In APIM, these are typically stored in named values or backends. So when creating components it is good practice to reuse these wherever these values will be environment-dependent. 

To create an environmental override for one of these values, add a record to the environment configuration file ie: configuration.prod.yaml. For example, to override a named value [nv--server-123] so that it's value is [server-dev] by default and [server-prod] in production, create a named value in the dev APIM instance with the default value and then create a new record in the configuration.prod.yaml file under named values.

'''
namedValues:
  - name: nv--server-123
    properties:
      displayName: nv--server-123
      value: "server-prod"
'''

To reference a key vault secret use:

'''
- name: mysecretvalue
    properties:
      displayName: mysecretvalue
      keyVault:
        identityClientId: [identity client id goes here]
        secretIdentifier: [your url here]
'''
