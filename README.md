# Create an ASP.NET Core application

## Task # 1
### Create an ASP.NET Core MVC. You may import use the following link to create a sample application
    https://docs.microsoft.com/en-us/aspnet/core/getting-started/?view=aspnetcore-5.0&tabs=windows

# Create Azure Pipeline

## Task # 2
1. Create Azure pipeline for the application using only powershell. Call this azure-pipeline-ps.yml


2. Create Azure pipeline for the application using ARM template(s). Call this azure-pipeline.yml

3. Both of these pipelines should have at least the following 4 stages. Each stage should have the listed jobs.

    Please note: Deployment should be based on Canary deployment pattern. You may decide to create additional stage(s), but not required.

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

All sensitive information should be stored in Azure DevOps variable groups and should be retrieved from their for configuration management.
