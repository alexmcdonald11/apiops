# APIOps Respository

Based on azure apiops: https://github.com/Azure/apiops


# About this tool

APIOps applies the concepts of DevOps to Azure API Management. This enables everyone involved in the lifecycle of API design, development, and deployment with self-service and automated tools to ensure the quality of the specifications and APIs that they're building. APIOps places the Azure API Management infrastructure under version control to achieve these goals. Rather than making changes directly in API Management portal, most operations happen through code changes that can be reviewed and audited. In this section, we include links to both a complementary Guide and Wiki to get you started with the tool.

Please bear in mind that APIOPS is designed to facilitate the promotion of changes across different Azure API Management (APIM) instances. While the animation below illustrates changes within the same instance, it's important to note that you can effortlessly apply your modifications across various Azure APIM instances using the supported configuration system. We advise taking some time to explore the wiki and documentation to grasp the functioning of configuration overrides when promoting changes across different environments.

![ApiOps](https://github.com/alexmcdonald11/apiops/assets/141607968/91660485-9fe6-47ed-8d2a-7be2ef5a6836)

# Setup

This tool relies on github environments so the repo must be a part of an **organizational account** or made **public** in order to use them.

1. Assuming two APIM environments (dev & prod), we need to create a github environment for each.
2. For each environment create and fill in the following secrets (use the Azure CLI to generate): API_MANAGEMENT_SERVICE_NAME, AZURE_CLIENT_ID, AZURE_CLIENT_SECRET, AZURE_RESOURCE_GROUP_NAME, AZURE_SUBSCRIPTION_ID, AZURE_TENANT_ID.
3. Configure appropriate protection rules for higher environment.
4. Create a configuration.prod.yaml file with the named higher environment instance.

A comprehensive guide can be found at: https://github.com/Azure/apiops/tree/main/docs/apiops/0-labPrerequisites


# Usage

1. Log in to the dev APIM instance and make required changes.
2. Log into github repository, go to actions and select Run-Extractor
3. Run workflow with default options
4. Approve / Merge auto-generated PR
5. Approve production deployment
6. Verify changes have propegated to prod

Test



