# Branching Strategy

Due to the unique setup of APIM, a slightly different branching strategy is recommended for managing APIs.

Once updates have been made in the development gui, the extrator workflow automatically creates a new branch and makes a new pull request to merge it back into main. The main branch can then be deployed into each environment independently using the GitHub environments configuration.




