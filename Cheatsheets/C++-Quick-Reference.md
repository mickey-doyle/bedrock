# C++ Quick Reference

## Program Structure
```cpp
#include <iostream>
using namespace std;

int main() {
    // Your code here
    return 0;
}
```

## Variables & Data Types
```cpp
// Basic types
int number = 42;
double decimal = 3.14;
float f = 3.14f;
char letter = 'A';
bool flag = true;
auto auto_var = "Type inferred";

// Constants
const int MAX_VALUE = 100;
constexpr int COMPILE_TIME = 200;

// References and Pointers
int& ref = number;         // Reference
int* ptr = &number;        // Pointer
int** ptr_to_ptr = &ptr;   // Pointer to pointer
```

## Memory Management
```cpp
// Dynamic allocation
int* array = new int[5];
delete[] array;

// Smart pointers (C++11)
#include <memory>
unique_ptr<int> unique(new int(42));
shared_ptr<int> shared = make_shared<int>(42);
weak_ptr<int> weak = shared;
```

## Control Flow
```cpp
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
while (condition) { }
do { } while (condition);

// Range-based for (C++11)
for (const auto& item : container) { }
```

## Functions
```cpp
// Basic function
int add(int a, int b) {
    return a + b;
}

// Function overloading
double add(double a, double b) {
    return a + b;
}

// Default parameters
void print(string msg = "Hello") { }

// Lambda expressions (C++11)
auto lambda = [](int x) { return x * 2; };

// Function templates
template<typename T>
T max(T a, T b) {
    return (a > b) ? a : b;
}
```

## Classes & Objects
```cpp
class Person {
private:
    string name;
    int age;

public:
    // Constructor
    Person(string n, int a) : name(n), age(a) { }
    
    // Virtual destructor
    virtual ~Person() { }
    
    // Member functions
    void setName(string n) { name = n; }
    string getName() const { return name; }
    
    // Pure virtual function
    virtual void speak() = 0;
};

// Inheritance
class Student : public Person {
public:
    Student(string n, int a) : Person(n, a) { }
    void speak() override { cout << "I am a student"; }
};
```

## Containers
```cpp
#include <vector>
#include <map>
#include <string>

// Vector
vector<int> vec = {1, 2, 3};
vec.push_back(4);

// Map
map<string, int> map;
map["key"] = 1;

// Array
array<int, 5> arr = {1, 2, 3, 4, 5};

// String
string str = "Hello";
str += " World";
```

## Exception Handling
```cpp
try {
    throw runtime_error("Error occurred");
} catch (const exception& e) {
    cerr << e.what() << endl;
} catch (...) {
    cerr << "Unknown error" << endl;
}
```

## Modern C++ Features (C++11 and beyond)
```cpp
// Auto type deduction
auto x = 42;

// Nullptr
int* ptr = nullptr;

// Range-based for
for (const auto& item : vector) { }

// Move semantics
string str1 = "Hello";
string str2 = move(str1);

// Initializer lists
vector<int> vec = {1, 2, 3, 4, 5};

// Structured bindings (C++17)
map<string, int> m = {{"one", 1}};
for (const auto& [key, value] : m) { }
```

## Input/Output
```cpp
// Console I/O
cout << "Output" << endl;
cin >> input;

// File I/O
#include <fstream>
ofstream outFile("file.txt");
outFile << "Writing to file";
outFile.close();

ifstream inFile("file.txt");
string content;
getline(inFile, content);
```
