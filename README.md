# github_actions

Each .yml file in  `.github/workflows` will create a Github Action.
Each action is/can be divided in jobs and each job is composed of steps.
A step can use a published github action **or** run commands

## Auto-Release  
The auto-release action is composed of 1 job, its steps are : 
- **Checkout** : checks out the repo so the wokflow can access it. Using `fetch-depth: 0` makes it fetch all history for all branches
- **Fetch commits**: performs `git log` to fetch all the commits being merged
- **Get current date**: Gets the current date to create the release's title
- **Create Release**: Creates the release with the above information
