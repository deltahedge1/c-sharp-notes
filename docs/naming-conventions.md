# Naming Conventions

## How Access Modifiers Work

| Naming Convention | Example | Case |
| --- | --- | --- |
| Classes | `Person`, `CustomerService`, `CarFactory` | PascalCase |
| Interfaces | `IComparable`, `IDisposable`, `IEnumerable` | IPascalCase |
| Local variables | `firstName`, `lastName`, `orderTotal` | camelCase |
| Private fields | `_firstName` or `fastName` | starts with `_` camelCase or without `_` |
| Constants | `MAX_RETRY_ATTEMPTS`, `ERROR_CODE_FILE_NOT_FOUND` | UPPERCASE_WITH_UNDERSCORES |
| Properties | `Name`, `Address`, `IsEnabled` | PascalCase (noun or noun phrase) |
| Methods | `Save`, `Delete`, `CalculateTotalCost` | PascalCase (verb or verb phrase) |

## Code

```C#
// Interface name should start with I
public interface IExampleInterface
{
    void DoSomething();
}

// Constant name should be all uppercase with underscores separating words
public static class ExampleConstants
{
    public const int MAX_COUNT = 100;
}

// Class name should be in PascalCase
public class ExampleClass
{
    // Private field name should start with an underscore and be in camelCase
    private string _exampleField;

    // Property name should be in PascalCase
    public string ExampleProperty { get; set; }

    // Method name should be in PascalCase
    public void ExampleMethod()
    {
        // Local variable name should be in camelCase
        int exampleVariable = 0;

        // Constant should be referenced using all uppercase with underscores separating words
        Console.WriteLine($"The maximum count is {ExampleConstants.MAX_COUNT}");
    }
}
```