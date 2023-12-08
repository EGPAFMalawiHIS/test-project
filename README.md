# test-project
This is just a test project to automate deployments of tags to other

# Push Tags to Destination Repo GitHub Action

This GitHub Action is designed to push tags from a source repository to a destination repository. It is triggered on any tag push to the source repository.

## Workflow Details

The workflow consists of three main steps:

1. **Checkout source repository**: This step checks out the source repository using the `actions/checkout@v4` action. It fetches all history for all tags and branches using `fetch-depth: 0`. The `token` used for checkout is a Personal Access Token (PAT) stored as a secret.

2. **Add destination repository as remote**: This step adds the destination repository as a remote repository using the `git remote add` command. The URL for the destination repository is stored as a secret.

3. **Push tags to destination repository**: This step pushes the tags from the source repository to the destination repository using the `git push` command. The tag name is obtained from the `github.ref_name` context.

## Setup

To use this workflow, you need to:

1. Copy the `push-tags.yml` file to the `.github/workflows` directory in your source repository.
2. Set up the following secrets in your source repository:
   - `PAT`: A Personal Access Token with the necessary permissions to checkout the source repository and push to the destination repository.
   - `DESTINATION_REPO_URL`: The URL of the destination repository.

Please note that this workflow runs on the latest version of Ubuntu.

## Usage

Once set up, this workflow will automatically run whenever a new tag is pushed to your source repository. It will push the same tag to the destination repository.# Push Tags to Destination Repo GitHub Action

This GitHub Action is designed to push tags from a source repository to a destination repository. It is triggered on any tag push to the source repository.

## Workflow Details

The workflow consists of three main steps:

1. **Checkout source repository**: This step checks out the source repository using the `actions/checkout@v4` action. It fetches all history for all tags and branches using `fetch-depth: 0`. The `token` used for checkout is a Personal Access Token (PAT) stored as a secret.

2. **Add destination repository as remote**: This step adds the destination repository as a remote repository using the `git remote add` command. The URL for the destination repository is stored as a secret.

3. **Push tags to destination repository**: This step pushes the tags from the source repository to the destination repository using the `git push` command. The tag name is obtained from the `github.ref_name` context.

## Setup

To use this workflow, you need to:

1. Copy the `push-tags.yml` file to the `.github/workflows` directory in your source repository.
2. Set up the following secrets in your source repository:
   - `PAT`: A Personal Access Token with the necessary permissions to checkout the source repository and push to the destination repository.
   - `DESTINATION_REPO_URL`: The URL of the destination repository.

Please note that this workflow runs on the latest version of Ubuntu.

## Usage

Once set up, this workflow will automatically run whenever a new tag is pushed to your source repository. It will push the same tag to the destination repository.
