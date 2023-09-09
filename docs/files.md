# Files in C#

## Write Files
```C#
string[] lines = {"first line", "second line", "third line"};
File.WriteAllLines("myFirstFile.txt", lines);
```

## Getting the current directory
```C#
Directory.GetCurrentDirectory();
```

## Getting the assembly location
```C#
typeof(program).Assembly.Location
//C:\Users\ihassan1\OneDrive - KPMG\Documents\AAA\csharpprojects\WordTemplating\bin\Debug\net6.0\WordTemplating.dll
```

## Resolving the Path
```C#
string basePath = Path.GetDirectoryName(typeof(Program).Assembly.Location) + @"/../..";
Console.WriteLine(Path.GetFullPath(basePath));
```