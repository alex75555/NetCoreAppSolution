# Simple blank NetCoreAppSolution


#Workflow

This workflow is defined in a YAML file and named "CI". It is triggered whenever a push event occurs on the main branch.

The workflow has a single job called "build" which runs on an Ubuntu virtual machine.

The job has five steps:

The actions/checkout@v2 action checks out the repository's code into the workflow's working directory.
The actions/setup-dotnet@v1 action sets up the .NET environment and installs the specified version of the .NET SDK.
The dotnet restore command restores the NuGet packages used by the project.
The dotnet build --no-restore command builds the project.
The dotnet test --no-build --verbosity normal command runs the project's tests.
