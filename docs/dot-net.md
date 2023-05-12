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
```terminal
dotnet add package <package_name> --version <version>
```

```terminal
dotnet add package Humanizer --version 2.7.9
```

```terminal
dotnet add package Humanizer --prerelease
```

## List packages

```terminal
dotnet list package
```

```terminal
dotnet list package --outdated
```

```terminal
dotnet list package --outdated --include-prerelease
```