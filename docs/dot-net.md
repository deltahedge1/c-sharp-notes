# .Net CLI

[tutorial](https://learn.microsoft.com/en-us/training/modules/dotnet-dependencies/3-exercise-dependency)


## List .Net SDKs
```terminal
dotnet --list-sdks
```

## Creating a new console app
```terminal
dotnet new console -h #help 
dotnet new console -n myProj2 -f net6.0
```

## Run the app 
```terminal
dotnet run
```

## Where are packages listed
```terminal
dotnet list packages
```
## Installing packages

## Project installation

```terminal
dotnet add package <package_name> --version <version>
```

```terminal
dotnet add package Humanizer --version 2.7.9
```

```terminal
dotnet add package Humanizer --prerelease
```

## Global installation

```terminal
dotnet add --global <reference>
```

## List packages

### Project packages
```terminal
dotnet list package
```

```terminal
dotnet list package --outdated
```

```terminal
dotnet list package --outdated --include-prerelease
```

### Global tools

```terminal
dotnet tool list --global
```

## Add a reference

```terminal
dotnet add reference path/to/MyLibrary.dll
```

## Creating a nuget package

```terminal
dotnet build
dotnet pack --configuration Relase // will package it to bin/Release/packagename.version.nupkg
dotnet nuget push <bin/Release/packagename.version.nupkg> --source https://api.nuget.org/v3/index.json --api-key <api_key>
```