# README for Azure Data Factory Deployment Workflow

This project contains a GitHub Actions workflow designed to automate the deployment of pipelines in Azure Data Factory. 

## Prerequisites

Before using this workflow, ensure you have the following:

- An Azure account with access to Azure Data Factory.
- A service principal with the necessary permissions to deploy resources in Azure Data Factory.
- The Azure CLI installed and configured on your local machine for testing purposes.

## Setup Instructions

1. **Clone the Repository**: 
   Clone this repository to your local machine using:
   ```
   git clone <repository-url>
   ```

2. **Configure Azure Credentials**:
   Set up your Azure credentials as GitHub Secrets. You will need to add the following secrets in your GitHub repository:
   - `AZURE_CLIENT_ID`: The client ID of your Azure service principal.
   - `AZURE_CLIENT_SECRET`: The client secret of your Azure service principal.
   - `AZURE_TENANT_ID`: The tenant ID of your Azure account.
   - `AZURE_SUBSCRIPTION_ID`: The subscription ID where your Azure Data Factory is located.
   - `DATA_FACTORY_NAME`: The name of your Azure Data Factory instance.

3. **Modify the Workflow**:
   Update the workflow file located at `.github/workflows/main.yml` if necessary to customize the deployment steps according to your pipeline requirements.

## Usage

Once the setup is complete, you can trigger the workflow by pushing changes to the `main` branch of your repository. The workflow will automatically authenticate with Azure and deploy the specified pipeline in Azure Data Factory.

## Example

To deploy a new pipeline, make changes to your pipeline definition files and push them to the `main` branch. The GitHub Actions workflow will handle the deployment process.

## Troubleshooting

If you encounter issues during deployment, check the Actions tab in your GitHub repository for logs and error messages. Ensure that your Azure credentials are correctly configured and that the service principal has the necessary permissions.

For further assistance, refer to the [Azure Data Factory documentation](https://docs.microsoft.com/en-us/azure/data-factory/introduction) or the [GitHub Actions documentation](https://docs.github.com/en/actions).
