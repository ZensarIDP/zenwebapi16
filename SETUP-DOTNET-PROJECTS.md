# zenwebapi16 Solution

This is a placeholder solution file. Replace this with your actual .NET solution file structure.

## Adding Your .NET Projects

1. **Remove this file** and add your actual solution file (`.sln`)
2. **Add your project directories** containing `.csproj` files
3. **Update the solution file** to reference all your projects
4. **Ensure one project is marked as the startup project** for the web application

## Multi-Project Structure Example

```
zenwebapi16/
├── zenwebapi16.sln
├── src/
│   ├── zenwebapi16.Api/
│   │   └── zenwebapi16.Api.csproj
│   ├── zenwebapi16.Core/
│   │   └── zenwebapi16.Core.csproj
│   └── zenwebapi16.Infrastructure/
│       └── zenwebapi16.Infrastructure.csproj
└── tests/
    └── zenwebapi16.Tests/
        └── zenwebapi16.Tests.csproj
```

## Docker Build

The included Dockerfile is designed to:
- Copy all files (including multiple projects)
- Run `dotnet restore` to restore all project dependencies
- Run `dotnet publish` which will automatically detect and build the startup project
- Create a runtime image with the published output

## GitHub Actions

The CI/CD workflow will:
- Build the Docker image with your multi-project solution
- Push to Google Container Registry
- Deploy to your selected target (Cloud Run or GKE)
