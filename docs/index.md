# C# notes

## Start a new project

1. open up visual studio
2. create a newproject and then name it


##  Printing to console
```C#
Console.WriteLine("hello world");
```

```C#
// To read a key input
string input = Console.ReadLine();
```

## Lists
```C#
List<int> myList = new List<int>;
var myOtherList = new List<int>;

myList.Add(1);
```

```C#
List<int> myList2 = new List<int> {1, 2, 5};
foreach (int i in myList2)
{
	Console.WriteLine(i);
}
```

## Arrays

```C#
dataType[] nameOfArray = new dataType[arraySize];
```

```C#
int[] myArray = new int[10]; // 10 is the size of the array
myArray[0] = 3;

int[] myOtherArray = {1, 2, 10, 7, 6}
Array.Sort(myOtherArray) // does it in place no need to assign
```

## Dictionary

```C#
Dictionary<string, int> scores = new Dictionary<String, int>();
scores.Add("Ish", 90);
scores.Add("Jane", 95);
scores.Add("Bob", 85);

foreach (var pair in scores)
{
	Console.WriteLine("{0} {1}", pair.Key, pair.Value);
}

```

```C#
Dictionary<string, int> scores = new Dictionary<string, int>();
scores.Add("John", 90);
scores.Add("Jane", 95);
scores.Add("Bob", 80);

foreach (KeyValuePair<string, int> pair in scores)
{
    Console.WriteLine("{0}: {1}", pair.Key, pair.Value);
}
```
## For loop

```C#
for(int i = 0, i <= 5, i++)
{
	Console.WriteLine(int);
}
```

## While loop

Not guaranteed to run atleast once like `do while`

```C#
int i = 0;
while(i <= 5)
{
	Console.Writeline(i);
	i += 1;
}
```

## Do while loop

guaranteed to run the first loop

```C#
int i = 0;

do
{
	Console.WriteLine(i);
} while ( i < 5);

```

## Reference vs Value Types

```C#
static void addOne(ref int num)
{
	Console.WriteLine($"value inside addOne {num}");
}

static void Main(string[] args)
{
	int num = 0;
	addOne(ref num);
	Console.WriteLine($"original value: {num}");
}
```

## Null coalescing

```C#
var a = variable ?? defaultVariable
```

```C#
Person person = null;
Person newPerson = person ?? new Person("Default", "Person");

Console.WriteLine(Person.FirstName);
```

## Constants vs readonly

| Constants      | Readonly    |
| :------------- | :---------- |
| Implicit static| Not implicit static |
| Constant must be initialised | Does not need to be initialised |
| Cannot hold custom types | Can hold custom types |

```C#
class Program
{
	public const string someText = "This is text";
	public static readonly string someOtherText = "Other text";

	static void Main(string[] args)
	{
		Console.WriteLine(someText);
	}
}
```

