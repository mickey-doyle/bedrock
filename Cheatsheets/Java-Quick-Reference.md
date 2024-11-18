# Java Quick Reference

## Basic Class Structure
```java
public class Main {
    public static void main(String[] args) { }
}
```

## Variables & Types
```java
int num = 5;                  // integer
String s = "text";           // string
double d = 5.0;              // double
char c = 'a';                // character
boolean flag = true;         // boolean
final int CONST = 1;         // constant
int[] arr = {1,2,3};         // array
var auto = "inferred";       // type inference
List<String> list = new ArrayList<>();  // list
```

## Control Flow
```java
if (x > 0) { } else { }

for (int i = 0; i < 10; i++) { }

while (condition) { }

for (String s : array) { }  // foreach

switch (var) { 
    case 1: break; 
    default: 
}
```

## Methods
```java
public static int add(int a, int b) { return a + b; }
void noReturn() { }
private String getName() { return name; }
```

## OOP
```java
class Dog extends Animal implements Interface {
    private String name;                // field
    public Dog(String name) { }         // constructor
    @Override public void speak() { }   // override
}
```

## Collections
```java
Map<K,V> map = new HashMap<>();     // key->value
Set<E> set = new HashSet<>();       // unique items
List<E> list = new ArrayList<>();   // ordered list
```

## Exceptions
```java
try {
    riskyCode();
} catch (Exception e) {
    handleError();
} finally {
    cleanup();
}
```

## Common Methods
```java
str.equals(str2)         // string compare
str.contains(sub)        // substring check
list.add(item)          // add to list
list.remove(idx)        // remove from list
map.put(key, val)       // add to map
map.get(key)            // get from map
```
