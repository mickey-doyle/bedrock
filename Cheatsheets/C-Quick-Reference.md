# C# Quick Reference

## Basic Structure
```csharp
namespace MyNamespace {
    class Program {
        static void Main(string[] args) {
            // Your code here
        }
    }
}
```

## Variables & Data Types
```csharp
// Basic types
int number = 42;
string text = "Hello";
bool flag = true;
char letter = 'A';
double decimal = 3.14;
var auto = "Type inferred";

// Constants
const int MAX_VALUE = 100;

// Nullable types
int? nullableNumber = null;
```

## Collections
```csharp
// Arrays
int[] numbers = new int[5];
string[] names = { "John", "Jane" };

// Lists
List<string> list = new List<string>();
list.Add("item");

// Dictionary
Dictionary<string, int> dict = new Dictionary<string, int>();
dict["key"] = 1;
```

## Control Flow
```csharp
// If statement
if (condition) {
    // code
} else if (otherCondition) {
    // code
} else {
    // code
}

// Switch
switch (value) {
    case 1:
        // code
        break;
    default:
        // code
        break;
}

// Loops
for (int i = 0; i < 10; i++) { }
foreach (var item in collection) { }
while (condition) { }
do { } while (condition);
```

## Methods
```csharp
// Basic method
public int Add(int a, int b) {
    return a + b;
}

// Expression bodied method
public int Multiply(int a, int b) => a * b;

// Generic method
public T GenericMethod<T>(T item) {
    return item;
}
```

## Classes & Objects
```csharp
public class Person {
    // Properties
    public string Name { get; set; }
    private int age;
    
    // Constructor
    public Person(string name) {
        Name = name;
    }
    
    // Method
    public void SayHello() {
        Console.WriteLine($"Hello, {Name}!");
    }
}

// Inheritance
public class Employee : Person {
    public Employee(string name) : base(name) { }
}
```

## LINQ (Language Integrated Query)
```csharp
var numbers = new List<int> { 1, 2, 3, 4, 5 };

// Query syntax
var query = from n in numbers
            where n > 2
            select n;

// Method syntax
var method = numbers.Where(n => n > 2)
                   .Select(n => n);
```

## Exception Handling
```csharp
try {
    // Risky code
    throw new Exception("Error");
} catch (Exception ex) {
    // Handle error
} finally {
    // Always executes
}
```


*Other Cheatsheets:*

[[C++-Quick-Reference]]
[[Java-Quick-Reference]]