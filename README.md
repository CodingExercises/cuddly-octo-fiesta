# Create an ASP.NET Core application

## Task # 1:
### Create an ASP.NET Core MVC. You may import use the following link to create a sample application or use an ASP.NET Core MVC application of your choice.
    https://docs.microsoft.com/en-us/aspnet/core/getting-started/?view=aspnetcore-5.0&tabs=windows

## Task # 2:
Add the following to appsettings.json file, if not already there
```
  "ConnectionStrings": {
    "DbConnection": ""
  }
```
# Create ADO Variable Groups

## Task # 3:
Add unique values to 'ConnectionString.DbConnection' variable in ADO variable groups for Dev, Stage and Production stages. Pick three GUID values for uniqueness.

# Create Azure Pipeline

## Task # 4:
1. Create Azure pipeline for the application using only powershell. Call this azure-pipeline-ps.yml

2. Create Azure pipeline for the application using ARM template(s). Call this azure-pipeline.yml

3. Both of these pipelines should have at least the following 4 stages. Each stage should have the listed jobs.

    Please note: You may decide to create additional stage(s) besides the required 4 stages.

        Build
            Restore
            Compile
            Run Tests
        
        Deployment to Dev
            Configure with Dev variables
            Deploy to Azure
        
        Deployment to Stage
            Configure with Staging variables
            Deploy to Azure
        
        Deployment to Production
            Configure with Production variables
            Deploy to Azure

All sensitive information should be stored in Azure DevOps variable groups and should be retrieved from their respective groups for configuration management.

Bonus credit: Implement Canary deployment pattern to the Production deployment stage.

Please email back to us when you are ready to submit. Email: watchguardengaccountowner@motorolasolutions.com

All the best!!!
