# Implementing a Class

## Pro Tips

### 1. ToString
In the `ToString` method you can get the class name using `this.GetType().Name`

```C#
public override string ToString()
{
    return $"{this.GetType().Name()} {this.X} {this.Y}"
}
```

### 2. Equals
In the `Equals` method good to implement two things

1. check if the other `object` is `null` or not the same object type
2. check if the properties are the same

```C#
public override bool Equals(object obj)
{
    if (obj == null || obj != GetType()) return false;
    return (this.X == obj.X) && (this.Y == obj.Y);
}
```

## Code

```C#
public class Person
{
    public string Name {get; set;};
    public int Age{get; set;};

    public Person(string name, int age)
    {
        this.Name = name;
        this.Age = age;
    }

    public override string ToString()
    {
        return $"class: {this.GetType().Name} name: {this.name} age: {this.name}"
    }

    public override bool Equal(object Obj)
    {
        if(obj == null || this.GetType() != obj.GetType())
        {
            return false;
        }

        Person p = (Person) obj;
        return (this.Name == p.Name) && (this.Age == p.Age);
    }

    public override int GetHashCode()
    {
        return (Name, Age).GetHasCode();
    }
}
```