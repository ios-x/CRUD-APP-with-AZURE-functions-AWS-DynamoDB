# CRUD APP with AZURE functions & AWS DynamoDB
This project showcases a serverless CRUD application that utilizes Azure and AWS technologies. The application can be deployed to an Azure function app or run locally.

# Technologies Used
* Azure Function App
* Azure Storage
* Amazon DynamoDB Table

# Project Structure
- `CreateFunction, DeleteFunction,GetFunction and UpdateFunction Folders` - Contains Code for the application's Azure functions.
- `local.settings.json` - A file which stores settings used by local development tools.
- `azuredeploy.json` - An ARM template in JSON format used to define and deploy an Azure Function App with associated services. The template defines the required resources, their dependencies, and configurations needed to create a function app implementation.
- `host.json` - this file defines the configuration code for the Azure Function Application.

## Guide for Local Deployment
When working with Azure function app locally in a project, ensure that any additional settings you add to `local.settings.json` must also be added to the function app in Azure since these settings are not automatically uploaded when publishing the project.
To run the application locally, please follow the guidelines below:

Ensure you have the following installed :
1. VS CODE([VS CODE](https://code.visualstudio.com/))
2. An Azure subscription. You can sign up for a free subscription [here](https://azure.microsoft.com/en-us/free/)
3. An AWS account. You can create an account [here](https://aws.amazon.com/resources/create-account/)
4. Azure Functions Core Tools installed. Follow the instructions [here](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=v4%2Cmacos%2Ccsharp%2Cportal%2Cbash#install-the-azure-functions-core-tools)
5. Node.js installed, including the npm package management tool. Download it from [here](https://nodejs.org/en/)
6. Azurite emulator installed. Follow the instructions [here](https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azurite)
7. Clone this repository to your local development machine.
8. Update the `local.settings.json` to reflect your DynamoDB Local credentials and table name.
9. Run the following script:
```bash
npm install aws-sdk
func start
```
10. Test the generated api using postman or any api tool you fill conformtable with.

## Deploy to Azure
1. [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fios-x%2Ftestappdeploy%2Fmain%2Fazuredeploy.json)
2. Clone this repository 
3. To deploy your functions to the function app, navigate to the Azure icon found in the explorer area in VS code
4. Go to the workspace area, select your project folder and select "Deploy" and choose "Deploy to Function App." You will be prompted to select the function app to which you want to deploy your functions.

5. Wait a few minutes for the deployment to complete, and once completed, you will see the message "Deployment succeeded".

* Finally, test your Function App by running it from the Azure portal or placing requests to its endpoint URL.

## Resources

* Learn more about [AWS DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html).
* Learn more about [Azure Functions](https://learn.microsoft.com/en-us/azure/azure-functions/).
