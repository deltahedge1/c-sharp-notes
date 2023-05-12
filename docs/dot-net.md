# .NET CLI

[tutorial](https://learn.microsoft.com/en-us/training/modules/dotnet-dependencies/3-exercise-dependency)


## List .Net SDKs
```.NET CLI
dotnet --list-sdks
```

## Creating a new console app
```.NET CLI
dotnet new console -h #help 
dotnet new console -n myProj2 -f net6.0
```

## Run the app 
```.NET CLI
dotnet run
```

## Where are packages listed
```.NET CLI
dotnet list packages
```
## Installing packages
```.NET CLI
dotnet add package <package_name> --version <version>
```

```.NET CLI
dotnet add package Humanizer --version 2.7.9
```

```.NET CLI
dotnet add package Humanizer --prerelease
```

## List packages

```.NET CLI
dotnet list package
```

```.NET CLI
dotnet list package --outdated
```

```.NET CLI
dotnet list package --outdated --include-prerelease
```
# DotNet CLI

## Under construction