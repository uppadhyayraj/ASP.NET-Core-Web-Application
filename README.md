# Testing an ASP.NET Core web application using .NET 6

This project is taken from specflow's repo to demostrate functionality of [Azure DevOps Testing Extension](https://marketplace.visualstudio.com/items?itemName=RajUppadhyay.ado-testingextension)


## Projects
This is sample/demo project to showcase following features of the [Azure DevOps Testing Extension](https://marketplace.visualstudio.com/items?itemName=RajUppadhyay.ado-testingextension):
- Create Tests from Feature Files to Azure DevOps, and if it is Dotnet Project then it automatically add the associated automation in DevOps. 
- Updating the test results to Associated Test Plan/Suites in Azure DevOps (Including Microsoft and Non-Microsoft testing frameworks)

### SpecFlowCalculator.Specs

A test project using the NUnit framework containing 5 simple example tests in [Calculator.feature](./SpecFlowCalculator.Specs/Features/Calculator.feature) and step definitions defined in [CalculatorStepDefinitions.cs](./SpecFlowCalculator.Specs/Steps/CalculatorStepDefinitions.cs)

## Notes

### Version

This project was built using .NET8 SDK version ```8.0.1```

## Getting Started

- Clone this repo into your local machine using your favorite IDE e.g. VS Code
- Check this code into your Azure Repo or Github repo
- Navigate to your Azure DevOps instance and [Craete a Test Plan](https://learn.microsoft.com/en-us/azure/devops/test/create-a-test-plan?view=azure-devops#create-a-test-plan) and note the ID of this
- Following the above link, also create a query based test suite with Tags Contains "myTag" and note the Id of this
- Also [Create a new Configuration](https://learn.microsoft.com/en-us/azure/devops/test/test-different-configurations?view=azure-devops&tabs=browser) and associate it with test suites created above. Please note the configuration ID for updating in YML in next steps
- Open the file [azure-pipelines.yml](./azure-pipelines.yml), as as commented in the YML file update the values/placeholder.
- [Create a pipeline](https://learn.microsoft.com/en-us/power-apps/maker/canvas-apps/test-studio-yaml-pipeline#create-a-pipeline) using above YML file and run it
- You will notice, test will populate automatically in above create test plan/test suites and also results being updated as well.
ß
