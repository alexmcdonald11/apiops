# Branching Strategy

When it comes to managing integration code using Git, a well-defined branching strategy is essential to ensure smooth collaboration, version control, and deployment of your integrations. A recommended branching strategy includes following branches.


## Main Branch
Maintain a main branch that always holds the stable and deployable version of the project. This branch represents the production-ready state of your code.


## Development Branch
Use a develop branch for ongoing development, serving as the base branch for features, fixes, and other enhancements. This branch should be regularly merged into main once the code is stable and ready for release.


## Feature Branches
Create feature branches from develop branch for new features or significant changes. Name these branches meaningfully, e.g., feature/add-login, to reflect the work being done. Merge them back into develop branch upon completion.

Naming Convention -> feature/branchName


## Hotfix Branches
For urgent fixes that need to be applied directly to the production environment, use hotfix branches created from main branch. Once the fix is tested and ready, merge it back into both main and develop.

Naming Convention -> hotfix/branchName
