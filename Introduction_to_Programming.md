# Introduction to Programming (C++)
## Variables & Data type
* int - Storing integers(whole numbers) 
* duble - Storing floating point numbers
* float - Storing floating point numbers
* char - Storing single chareters
* bool - Storing values with two stages : true or false
* string - Storing text

### Example :
```c++
int a = 10;
double b = 10.10;
float c = 4.54;
char d = 'r';
bool e = 1;
string f = "Md Rijoan Maruf";
```
## Rules of variable names:
* Name must begin with a letter or underscore ( _ ) and can be followed by any combination of letters, underscores, or digits. 
* Key word cannot be used.

## Output :
```c++
cout << "Hello World!" << endl;
```
* endl --> New line


## Comments :
```c++
// This is single line comment
/* This is multi 
        line comments */
```


## User Input :
```c++
int x;
cin >> x;   // Get the user input from the keyboard. and store in x;
```
## Operators :
### Arithmetic Operators :

    +   | Addition | adds together two vvalues
    -   | Subtruct | Subtracts one value from another	
    *   | Multiplication | Multiplies two values	
    /   | Division | Divides one value by another	
    %   | Modulus  | Returns the division remainder	
    ++  | Increment | Increases the value of a variable by 1	
    --  | Derement  | Decreases the value of a variable by 1	


### Assignment Operators :
    +=	|  x += 3	|  x = x + 3	
    -=	|  x -= 3	|  x = x - 3	
    *=	|  x *= 3	|  x = x * 3	
    /=	|  x /= 3	|  x = x / 3	
    %=	|  x %= 3	|  x = x % 3	
    &=	|  x &= 3	|  x = x & 3	
    |=	|  x |= 3	|  x = x | 3	
    ^=	|  x ^= 3	|  x = x ^ 3	
    >>=	|  x >>= 3	|  x = x >> 3	
    <<=	|  x <<= 3	|  x = x << 3	

### Comparison Operators :
    ==	|  Equal to	                 x == y	
    !=	|  Not equal	             x != y	
    >	|  Greater than	             x > y	
    <	|  Less than	             x < y	
    >=	|  Greater than or equal to	 x >= y	
    <=	|  Less than or equal to	 x <= y

### Logical Operators :
    && 	|  Logical and	|  Returns true if both statements are true	
    || 	|  Logical or	|  Returns true if one of the statements is true	
    !	|  Logical not	|  Reverse the result, returns false if the result is true	

## String :

```c++
// Include the string library
#include <string>

// Create a string variable
string a = "Hello";
```

### Concatenation :
```c++
string firstName = "Rijoan ";
string lastName = "Maruf";
string fullName = firstName + lastName;
cout << fullName << endl;
// Now fullName = "Rijoan Maruf" ;
```


### Append :
```c++
string firstName = "Rijoan ";
string lastName = "Maruf";
string fullName = firstName.append(lastName);
cout << fullName << endl;
// Now fullName = "Rijoan Maruf" ;
```


### String lenght() :
```c++
string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
cout << "The length of the txt string is: " << txt.length();
```


### String size() :
```c++
string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
cout << "The length of the txt string is: " << txt.size();
```


### Access String :
You can access string with index. And the index start with zero.
```c++
cout << myString[0];
// Outputs H
```


### Special Charecters :

    Escape characte	    Resuls      Decription
    \'	                '	        Single quote
    \"	                "	        Double quote
    \\	                \	        Backslash
    \n                  New line
    \t                  Tab


### User Input String :

```c++
string firstName;
cout << "Type your first name: ";
cin >> firstName; // get user input from the keyboard
cout << "Your name is: " << firstName;

// Type your first name: Rijoan
// Your name is: Rijoan
```
**Note** : cin considers a space (whitespace, tabs, etc) as a terminating character, which means that it can only store a single word (even if you type many words)

## Math :
### max() , min() :
```c++

cout << max(5, 10); // Output : 10
cout << min(5, 10); // Output : 5
```

```c++
// Include the cmath library
#include <cmath>

cout << sqrt(64);       // 8
cout << round(2.6);     // 2
cout << log(2);         // 0.693147
```

    pow(x,y)	Returns the value of x to the power of y
    sin(x)	    Returns the sine of x (x is in radians)
    sinh(x)	    Returns the hyperbolic sine of a double value
    tan(x)	    Returns the tangent of an angle
    tanh(x)	    Returns the hyperbolic tangent of a double value

## Booleans :
```c++
bool a = true;
bool b = false;
cout << a;  // Outputs 1 (true)
cout << b;  // Outputs 0 (false)
```

## Boolean Expression :
```c++
int x = 10;
int y = 9;
cout << (x > y); // returns 1 (true), because 10 is higher than 9
```

```c++
cout << (10 == 15);  // returns 0 (false), because 10 is not equal to 15
int x = 10;
cout << (x == 10);  // returns 1 (true), because the value of x is equal to 10
```

## Conditions :
```c++
int time = 22;
if (time < 10) {
  cout << "Good morning.";
} else if (time < 20) {
  cout << "Good day.";
} else {
  cout << "Good evening.";
}
// Outputs "Good evening."
```

### Shorthand if..else :
```c++
int time = 20;
string result = (time < 18) ? "Good day." : "Good evening.";
cout << result;
```

## Switch :
```c++
int day = 4;
switch (day) {
  case 1:
    cout << "Monday";
    break;
  case 2:
    cout << "Tuesday";
    break;
  case 3:
    cout << "Wednesday";
    break;
  case 4:
    cout << "Thursday";
    break;
  case 5:
    cout << "Friday";
    break;
  case 6:
    cout << "Saturday";
    break;
  case 7:
    cout << "Sunday";
    break;
}
// Outputs "Thursday" (day 4)
```

## While Loop :
```c++
int i = 0;
while (i < 5) {
  cout << i << "\n";
  i++;
}
```

## Do/While Loop :
```c++
do {
  cout << i << "\n";
  i++;
}
while (i < 5);
```

## For Loop :
```c++
for (int i = 0; i < 5; i++) {
  cout << i << "\n";
}
```

## Break/Continue :
```c++
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    break;
  }
  cout << i << "\n";
}
// Break Full loop
```

```c++
  if (i == 4) {
    continue;
  }
  cout << i << "\n";
}
// Break 1 Loop
```

## Arrays :
```c++
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
cout << cars[0];
// Outputs Volvo
```

```c++
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
cout << cars[0];
// Now outputs Opel instead of Volvo
```

### Loop in Array :
```c++
string cars[5] = {"Volvo", "BMW", "Ford", "Mazda", "Tesla"};
for (int i = 0; i < 5; i++) {
  cout << cars[i] << "\n";
}
```
### Omit Array Size :
```c++
string cars[] = {"Volvo", "BMW", "Ford"}; // Three array elements
string cars[3] = {"Volvo", "BMW", "Ford"}; // Also three array elements
```

### Size of an Array :
```c++
int num[5] = {10, 20, 30, 40, 50};
cout << sizeof(num);
// Output : 20 Becaus every element is 4 byte
```

```c++
int myNumbers[5] = {10, 20, 30, 40, 50};
int getArrayLength = sizeof(myNumbers) / sizeof(int);
cout << getArrayLength;
```

### Loop Through an Array with sizeof() :
```c++
int myNumbers[5] = {10, 20, 30, 40, 50};
for (int i = 0; i < sizeof(myNumbers) / sizeof(int); i++) {
  cout << myNumbers[i] << "\n";
}
```

### for-each Loop :
```c++
int myNumbers[5] = {10, 20, 30, 40, 50};
for (int i : myNumbers) {
  cout << i << "\n";
}
```

## Multidimenstional Arrays :
**2D**
```c++
string letters[2][4] = {
  { "A", "B", "C", "D" },
  { "E", "F", "G", "H" }
};
```

**3D**
```c++
string letters[2][2][2] = {
  {
    { "A", "B" },
    { "C", "D" }
  },
  {
    { "E", "F" },
    { "G", "H" }
  }
};
```

## Structures (struct) :
```c++
// Create a structure variable called myStructure
struct {
  int myNum;
  string myString;
} myStructure;

// Assign values to members of myStructure
myStructure.myNum = 1;
myStructure.myString = "Hello World!";

// Print members of myStructure
cout << myStructure.myNum << "\n";
cout << myStructure.myString << "\n";
```

```c++
struct {
  string brand;
  string model;
  int year;
} myCar1, myCar2; // We can add variables by separating them with a comma here

// Put data into the first structure
myCar1.brand = "BMW";
myCar1.model = "X5";
myCar1.year = 1999;

// Put data into the second structure
myCar2.brand = "Ford";
myCar2.model = "Mustang";
myCar2.year = 1969;

// Print the structure members
cout << myCar1.brand << " " << myCar1.model << " " << myCar1.year << "\n";
cout << myCar2.brand << " " << myCar2.model << " " << myCar2.year << "\n";
```

### Named Structures :
By giving a name to the structure, you can treat it as a data type. This means that you can create variables with this structure anywhere in the program at any time.
To create a named structure, put the name of the structure right after the struct keyword:
```c++
// Declare a structure named "car"
struct car {
  string brand;
  string model;
  int year;
};

int main() {
  // Create a car structure and store it in myCar1;
  car myCar1;
  myCar1.brand = "BMW";
  myCar1.model = "X5";
  myCar1.year = 1999;

  // Create another car structure and store it in myCar2;
  car myCar2;
  myCar2.brand = "Ford";
  myCar2.model = "Mustang";
  myCar2.year = 1969;
 
  // Print the structure members
  cout << myCar1.brand << " " << myCar1.model << " " << myCar1.year << "\n";
  cout << myCar2.brand << " " << myCar2.model << " " << myCar2.year << "\n";
 
  return 0;
}
```

### Reference Variable :
A reference variable is a "reference" to an existing variable, and it is created with the & operator.
```c++
string food = "Pizza";
string &meal = food;

// Now, we can use either the variable name food or the reference name meal to refer to the food variable.
cout << food << "\n";  // Outputs Pizza
cout << meal << "\n";  // Outputs Pizza
```

### Memory Address :
```c++
string food = "Pizza";

cout << &food; // Outputs 0x6dfed4
```

## Pointers :
```c++
string food = "Pizza";  // A food variable of type string
string* ptr = &food;    // A pointer variable, with the name ptr, that stores the address of food

// Output the value of food (Pizza)
cout << food << "\n";

// Output the memory address of food (0x6dfed4)
cout << &food << "\n";

// Output the memory address of food with the pointer (0x6dfed4)
cout << ptr << "\n";
```

## De-reference :
**Get Memory Address and Value :**
```c++
string food = "Pizza";  // Variable declaration
string* ptr = &food;    // Pointer declaration

// Reference: Output the memory address of food with the pointer (0x6dfed4)
cout << ptr << endl;

// Dereference: Output the value of food with the pointer (Pizza)
cout << *ptr << endl;
```

### Modify the Pointer Value :
```c++
string food = "Pizza";
string* ptr = &food;

// Output the value of food (Pizza)
cout << food << endl;

// Output the memory address of food (0x6dfed4)
cout << &food << endl;

// Access the memory address of food and output its value (Pizza)
cout << *ptr << endl;

// Change the value of the pointer
*ptr = "Hamburger";

// Output the new value of the pointer (Hamburger)
cout << *ptr << endl;

// Output the new value of the food variable (Hamburger)
cout << food << endl;
```

## Function :
### Create a Function :
```c++
void myFunction() {
  // code to be executed
}
```
* myFunction() is the name of the function.
* void means that the function does not have a return value. 
* Inside the function (the body), add code that defines what the function should do.
* A function can be called muliple times.

### Call a Function :
```c++
// Create a function
void myFunction() {
  cout << "Hello World!" << endl;
}

int main() {
  myFunction(); // call the function
  return 0;
}
// Outputs "I just got executed!"
```

Function can be declear first and definition later.
```c++
// Function declaration
void myFunction();

// The main method
int main() {
  myFunction();  // call the function
  return 0;
}

// Function definition
void myFunction() {
  cout << "I just got executed!";
}
```

### Parameters and Arguments
```c++
void myFunction(string fname) {
  cout << "Md. " << fname << endl ;
}

int main() {
  myFunction("Rijoan");
  myFunction("Rihan");
  myFunction("Srabon");
  return 0;
}

// Md. Rijoan
// Md. Rihan
// Md. Srabon
```

### Defalut Parameter Value :

```c++
void myFunction(string country = "Bangladesh") {
  cout << country << "\n";
}

int main() {
  myFunction("Sweden");
  myFunction("India");
  myFunction();         // it will print "Bangladesh" as a default parameter.
  myFunction("USA");
  return 0;
}

// Sweden
// India
// Bangladesh
// USA
```

### Return Values :
```c++
int myFunction(int x) {
  return 5 + x;
}

int main() {
  cout << myFunction(3);
  return 0;
}

// Outputs 8 (5 + 3)
```

## Pass By Reference
Change orignal Values by reference.
```c++
void swapNums(int &x, int &y) {
  int z = x;
  x = y;
  y = z;
}

int main() {
  int firstNum = 10;
  int secondNum = 20;

  cout << "Before swap: " << "\n";
  cout << firstNum << secondNum << "\n";

  // Call the function, which will change the values of firstNum and secondNum
  swapNums(firstNum, secondNum);

  cout << "After swap: " << "\n";
  cout << firstNum << secondNum << "\n";

  return 0;
}
```

### Pass Arrays as Function Parameters :
```c++
void myFunction(int myNumbers[5]) {
  for (int i = 0; i < 5; i++) {
    cout << myNumbers[i] << "\n";
  }
}

int main() {
  int myNumbers[5] = {10, 20, 30, 40, 50};
  myFunction(myNumbers);
  return 0;
}
```

### Fucntion Overloading :
With function overloading, multiple functions can have the same name with different parameters.
```c++
int plusFuncInt(int x, int y) {
  return x + y;
}

double plusFuncDouble(double x, double y) {
  return x + y;
}

int main() {
  int myNum1 = plusFuncInt(8, 5);
  double myNum2 = plusFuncDouble(4.3, 6.26);
  cout << "Int: " << myNum1 << "\n";
  cout << "Double: " << myNum2;
  return 0;
}
```

## Recursion :
Recursion is the technique of making a function call itself. This technique provides a way to break complicated problems down into simple problems which are easier to solve.
```c++
#include <iostream>

using namespace std;

unsigned int factorial(unsigned int n) {
  if (n == 0 || n == 1) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

int main() {
  unsigned int num;
  cout << "Enter a number: ";
  cin >> num;

  cout << "Factorial of " << num << " is " << factorial(num) << endl;

  return 0;
}
```


## Object Oriented Programming
* OOP is faster and easier to execute
* OOP provides a clear structure for the programs
* OOP helps to keep the C++ code DRY "Don't Repeat Yourself", and makes the code easier to maintain, modify and debug
* OOP makes it possible to create full reusable applications with less code and shorter development time
**Example :** 

``` 
Class -> Fruit
Objects -> Apple , Banana , Mango etc

Class -> Car
Objects -> Volvo , Audi , Toyota , Marcities , BMW etc
```

## Classes / Objects :
```c++
class MyClass {       // The class
  public:             // Access specifier
    int myNum;        // Attribute (int variable)
    string myString;  // Attribute (string variable)
};

int main() {
  MyClass myObj;  // Create an object of MyClass

  // Access attributes and set values
  myObj.myNum = 15; 
  myObj.myString = "Some text";

  // Print attribute values
  cout << myObj.myNum << "\n";
  cout << myObj.myString;
  return 0;
}
```

### Multiple Objects :
```c++
// Create a Car class with some attributes
class Car {
  public:
    string brand;   
    string model;
    int year;
};

int main() {
  // Create an object of Car
  Car carObj1;
  carObj1.brand = "BMW";
  carObj1.model = "X5";
  carObj1.year = 1999;

  // Create another object of Car
  Car carObj2;
  carObj2.brand = "Ford";
  carObj2.model = "Mustang";
  carObj2.year = 1969;

  // Print attribute values
  cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";
  cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";
  return 0;
}
```

## Class Methods :
There are two ways to define functions that belongs to a class:

* Inside class definition
* Outside class definition

**Inside Class Example :**
```c++
class MyClass {        // The class
  public:              // Access specifier
    void myMethod() {  // Method/function defined inside the class
      cout << "Hello World!";
    }
};

int main() {
  MyClass myObj;     // Create an object of MyClass
  myObj.myMethod();  // Call the method
  return 0;
}
```

**Outside Class Example :**
```c++
  public:              // Access specifier
    void myMethod();   // Method/function declaration
};

// Method/function definition outside the class
void MyClass::myMethod() {
  cout << "Hello World!";
}

int main() {
  MyClass myObj;     // Create an object of MyClass
  myObj.myMethod();  // Call the method
  return 0;
}
```

### Method/Function Perameters :
```c++
#include <iostream>
using namespace std;

class Car {
  public:
    int speed(int maxSpeed);
};

int Car::speed(int maxSpeed) {
  return maxSpeed;
}

int main() {
  Car myObj; // Create an object of Car
  cout << myObj.speed(200); // Call the method with an argument
  return 0;
}
```

## Constructors :
A constructor in C++ is a special method that is automatically called when an object of a class is created.

```c++
#include <iostream>
using namespace std;

class MyClass {     // The class
  public:           // Access specifier
    MyClass() {     // Constructor
      cout << "Hello World!";
    }
};

int main() {
  MyClass myObj;    // Create an object of MyClass (this will call the constructor)
  return 0;
}
```

### Constructor Parameters :
Constructors can also take parameters (just like regular functions), which can be useful for setting initial values for attributes.


```c++
#include <iostream>
using namespace std;

class Car {        // The class
  public:          // Access specifier
    string brand;  // Attribute
    string model;  // Attribute
    int year;      // Attribute
    Car(string x, string y, int z) {  // Constructor with parameters
      brand = x;
      model = y;
      year = z;
    }
};

int main() {
  // Create Car objects and call the constructor with different values
  Car carObj1("BMW", "X5", 1999);
  Car carObj2("Ford", "Mustang", 1969);

  // Print values
  cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";
  cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";
  return 0;
}
```
**Output :**
```c++
BMW X5 1999
Ford Mustang 1969
```

## Access Specifiers :
**There are three access specifiers :**

* public - Members are accessible from outside the class
* private - Members cannot be accessed (or viewed) from outside the class
* protected - Members cannot be accessed from outside the class, however, they can be accessed in inherited classes
```c++
class MyClass {
  public:    // Public access specifier
    int x;   // Public attribute
  private:   // Private access specifier
    int y;   // Private attribute
};

int main() {
  MyClass myObj;
  myObj.x = 25;  // Allowed (public)
  myObj.y = 50;  // Not allowed (private)
  return 0;
}
```
**Output :**

    error: y is private

## Encapsulation :
* Encapsulation helps in reducing the complexity of code.
* Encapsulation helps in hiding data protecting the data.
* Encapsulated class are easy to alter using the access modifier.


### Access Private Members
```c++
#include <iostream>
using namespace std;

class Employee {
  private:
    // Private attribute
    int salary;

  public:
    // Setter
    void setSalary(int s) {
      salary = s;
    }
    // Getter
    int getSalary() {
      return salary;
    }
};

int main() {
  Employee myObj;
  myObj.setSalary(50000);
  cout << myObj.getSalary();
  return 0;
}
```
**Example explained :**

    The salary attribute is private, which have restricted access.  
    The public setSalary() method takes a parameter (s) and assigns it to the salary attribute (salary = s).  
    The public getSalary() method returns the value of the private salary attribute.  
    Inside main(), we create an object of the Employee class. Now we can use the setSalary() method to set the  value of the private attribute to 50000. Then we call the getSalary() method on the object to return the  value.

## Inheritance :
In C++, it is possible to inherit attributes and methods from one class to another. 
* **Derived class** (child) - the class that inherits another calss
* **Base class** (parent) - the class beling inherited from


```c++
// Base class
class Vehicle {
  public:
    string brand = "Ford";
    void honk() {
      cout << "Tuut, tuut! \n" ;
    }
};

// Derived class
class Car: public Vehicle {
  public:
    string model = "Mustang";
};

int main() {
  Car myCar;
  myCar.honk();
  cout << myCar.brand + " " + myCar.model;
  return 0;
}
```
In the example, the Car class (child) inherits the attributes and methods from the Vehicle class (parent).


### Multilevel Inheritance :
A class can also be derived from one class, which is already derived from another class.
In the following example, MyGrandChild is derived from class MyChild (which is derived from MyClass).

```c++
int main() {
  MyGrandChild myObj;
  myObj.myFunction();
  return 0;
}
```

### Multiple Inheriance :
A class can also be derived from more than one base class, using a comma-separated list.
```c++
class MyClass {
  public:
    void myFunction() {
      cout << "Some content in parent class." ;
    }
};

// Another base class
class MyOtherClass {
  public:
    void myOtherFunction() {
      cout << "Some content in another class." ;
    }
};

// Derived class
class MyChildClass: public MyClass, public MyOtherClass {
};

int main() {
  MyChildClass myObj;
  myObj.myFunction();
  myObj.myOtherFunction();
  return 0;
}
```

### Access Specifiers :
* **public** : Members of a class are accessible from outside the class
* **private** : Members can only be accessed within the class
* **protected** : Protected, is similar to private, but it can also be accessed in the inherited class
```c++
// Base class
class Employee {
  protected: // Protected access specifier
    int salary;
};

// Derived class
class Programmer: public Employee {
  public:
    int bonus;
    void setSalary(int s) {
      salary = s;
    }
    int getSalary() {
      return salary;
    }
};

int main() {
  Programmer myObj;
  myObj.setSalary(50000);
  myObj.bonus = 15000;
  cout << "Salary: " << myObj.getSalary() << "\n";
  cout << "Bonus: " << myObj.bonus << "\n";
  return 0;
}
```

## Polymorphism :
Polymorphism means "many forms", and it occurs when we have many classes that are related to each other by inheritance.

```c++
// Base class
class Animal {
  public:
    void animalSound() {
      cout << "The animal makes a sound \n";
    }
};

// Derived class
class Pig : public Animal {
  public:
    void animalSound() {
      cout << "The pig says: wee wee \n";
    }
};

// Derived class
class Dog : public Animal {
  public:
    void animalSound() {
      cout << "The dog says: bow wow \n";
    }
};
```
```c++
// Base class
class Animal {
  public:
    void animalSound() {
      cout << "The animal makes a sound \n";
    }
};

// Derived class
class Pig : public Animal {
  public:
    void animalSound() {
      cout << "The pig says: wee wee \n";
    }
};

// Derived class
class Dog : public Animal {
  public:
    void animalSound() {
      cout << "The dog says: bow wow \n";
    }
};

int main() {
  Animal myAnimal;
  Pig myPig;
  Dog myDog;

  myAnimal.animalSound();
  myPig.animalSound();
  myDog.animalSound();
  return 0;
}
```

## Files :
The fstream library allows us to work with files.
To use the **fstream** library, include both the standard **iostream** AND the **fstream** header file.

* **ofstream**	Creates and writes to files
* **ifstream**	Reads from files
* **fstream**	A combination of ofstream and ifstream: creates, reads, and writes to files

### Create and Write to a File :
To create a file, use either the **ofstream** or **fstream** class, and specify the name of the file.

```c++
#include <iostream>
#include <fstream>
using namespace std;

int main() {
  // Create and open a text file
  ofstream MyFile("filename.txt");

  // Write to the file
  MyFile << "Files can be tricky, but it is fun enough!";

  // Close the file
  MyFile.close();
}
```

### Read a File :
To read from a file, use either the **ifstream** or **fstream** class, and the name of the file.
**Note :** We also use a **while** loop together with the **getline()** function (which belongs to the **ifstream** class) to read the file line by line, and to print the content of the file.

```c++
// Create a text string, which is used to output the text file
string myText;

// Read from the text file
ifstream MyReadFile("filename.txt");

// Use a while loop together with the getline() function to read the file line by line
while (getline (MyReadFile, myText)) {
  // Output the text from the file
  cout << myText;
}

// Close the file
MyReadFile.close();
```

## Exceptions :
* When executing C++ code, different errors can occur: coding errors made by the programmer, errors due to wrong input, or other unforeseeable things.
* When an error occurs, C++ will normally stop and generate an error message. The technical term for this is: C++ will throw an exception (throw an error)


### try and catch :
Exception handling in C++ consist of three keywords: **try**, **throw** and **catch**.
* The try statement allows you to define a block of code to be tested for errors while it is being executed.
* The throw keyword throws an exception when a problem is detected, which lets us create a custom error.
* The catch statement allows you to define a block of code to be executed, if an error occurs in the try block.

```c++
try{
  // Block of code to try
  throw exception; // Throw an exception when a problem arise
}
catch () {
  // Block of code to handle errors
}
```

```c++
try {
  int age = 15;
  if (age >= 18) {
    cout << "Access granted - you are old enough.";
  } else {
    throw (age);
  }
}
catch (int myNum) {
  cout << "Access denied - You must be at least 18 years old.\n";
  cout << "Age is: " << myNum;
}
```

```c++
try {
  int age = 15;
  if (age >= 18) {
    cout << "Access granted - you are old enough.";
  } else {
    throw 505;
  }
}
catch (int myNum) {
  cout << "Access denied - You must be at least 18 years old.\n";
  cout << "Error number: " << myNum;
}
```





