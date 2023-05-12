## Access Modifiers

| Access Modifier | Visibility |
| --- | --- |
| `public` | The type or member can be accessed from anywhere. |
| `private` | The type or member can only be accessed from within the same class. |
| `internal` | The type or member can only be accessed from within the same assembly. |
| `protected` | The type or member can only be accessed from within the same class or a derived class. |
| `protected internal` | The type or member can only be accessed from within the same assembly or a derived class in another assembly. |
| `private protected` | The type or member can only be accessed from within the same assembly and from any derived class in the same assembly. |


```C#
// This is a public class that can be accessed from anywhere.
public class PublicClass
{
    // This is a public field that can be accessed from anywhere.
    public int PublicField;

    // This is a public method that can be accessed from anywhere.
    public void PublicMethod()
    {
        // Implementation code goes here.
    }

    // This is a private method that can only be accessed from within this class.
    private void PrivateMethod()
    {
        // Implementation code goes here.
    }

    // This is an internal method that can only be accessed from within this assembly.
    internal void InternalMethod()
    {
        // Implementation code goes here.
    }

    // This is a protected method that can only be accessed from within this class or a derived class.
    protected void ProtectedMethod()
    {
        // Implementation code goes here.
    }

    // This is a protected internal method that can be accessed from within this assembly or a derived class in another assembly.
    protected internal void ProtectedInternalMethod()
    {
        // Implementation code goes here.
    }

    // This is a private protected method that can only be accessed from within this assembly and from any derived class in the same assembly.
    private protected void PrivateProtectedMethod()
    {
        // Implementation code goes here.
    }
}

// This is a class that derives from PublicClass and can access its protected and protected internal members.
public class DerivedClass : PublicClass
{
    public void AccessProtectedMembers()
    {
        ProtectedMethod();
        ProtectedInternalMethod();
    }
}

// This is a class in a different assembly that can only access PublicClass's public and protected internal members.
public class ExternalClass
{
    public void AccessPublicMembers(PublicClass obj)
    {
        obj.PublicField = 42;
        obj.PublicMethod();
        obj.ProtectedInternalMethod(); // This is allowed because it's protected internal.
        // obj.PrivateMethod(); // This is not allowed because it's private.
        // obj.InternalMethod(); // This is not allowed because it's internal.
        // obj.PrivateProtectedMethod(); // This is not allowed because it's private protected.
    }
}
```