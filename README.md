# Incorporating Workflows in Your Repositories

This guide will walk you through the steps to integrate workflows into your repositories. Follow these instructions carefully to ensure proper setup and customization.

## Step 1: Directory Structure
To begin, refer to the directory structure in our [example repository](https://github.com/Ambibuzz/.github). It showcases the recommended setup for the `.github` folder.

### Action:
- Create a `.github` directory in the root of your repository.
- Inside `.github`, create the necessary subdirectories (such as `workflows`, `scripts`, etc.) to match the structure in the example.

## Step 2: Add Environment Secrets
For the workflows to function properly, you need to store some sensitive information securely in the repository secrets.

### Action:
1. Go to your GitHub repository’s **Settings**.
2. Under **Security**, click on **Secrets and variables** → **Actions**.
3. Click the **New repository secret** button.
4. Add the following secrets:
   - **CLOUD_FUNCTION_URL**: The URL of your cloud function (Value = `value-from-keep`).
   - **FUNCTION_API_KEY**: Your API key (Value = `value-from-keep`).

These secrets are essential for the workflows to interact with external services securely.

## Step 3: Add the `.flake8` Configuration
Flake8 is a tool for enforcing Python code style standards. We recommend adding a `.flake8` configuration file to your repository's root directory.

### Action:
1. In the root of your repository, create a `.flake8` file.
2. You can customize the configuration as needed to align with your project’s code style.

For example, a basic `.flake8` file could look like [this](https://github.com/Ambibuzz/.github/blob/development/.flake8).

This configuration will set the maximum line length to 120 characters and exclude certain directories from linting.

## Step 4: Customize Workflow Files (Optional)
The workflows provided are designed to automate key processes, but you can adjust them according to your project’s needs.

### Action:
1. Go through the `.github/workflows` directory and inspect the workflow files.
2. Make any necessary adjustments, such as modifying job steps, adding additional steps, or changing environment variables.

