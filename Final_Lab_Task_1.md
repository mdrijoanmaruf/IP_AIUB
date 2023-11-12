# Lab task - 1 (Pointer)
## 1. Take 5 variables and print Variable Addresses
```c++
#include <iostream>

using namespace std;

int main() {
    // Declare variables
    int a, b, c;
    double x, y;

    // Print addresses of variables
    cout << "Address of variable a: " << &a << endl;
    cout << "Address of variable b: " << &b << endl;
    cout << "Address of variable c: " << &c << endl;
    cout << "Address of variable x: " << &x << endl;
    cout << "Address of variable y: " << &y << endl;

    return 0;
}
```
### Output :
    Address of variable a: 0x7ffd8c51069c
    Address of variable b: 0x7ffd8c5106a0
    Address of variable c: 0x7ffd8c5106a4
    Address of variable x: 0x7ffd8c5106a8
    Address of variable y: 0x7ffd8c5106b0

## 2. Take 5 variables and print Variable Addresses by using pointer
```c++
#include <iostream>

using namespace std;

int main() {
    // Declare variables
    int a, b, c;
    double x, y;

    // Declare pointers
    int *ptr_a = &a;
    int *ptr_b = &b;
    int *ptr_c = &c;
    double *ptr_x = &x;
    double *ptr_y = &y;

    // Print addresses of variables using pointers
    cout << "Address of variable a: " << ptr_a << endl;
    cout << "Address of variable b: " << ptr_b << endl;
    cout << "Address of variable c: " << ptr_c << endl;
    cout << "Address of variable x: " << ptr_x << endl;
    cout << "Address of variable y: " << ptr_y << endl;

    return 0;
}
```
### Output :
    Address of variable a: 0x7fff15a0e374
    Address of variable b: 0x7fff15a0e378
    Address of variable c: 0x7fff15a0e37c
    Address of variable x: 0x7fff15a0e380
    Address of variable y: 0x7fff15a0e388

## 3. Take 5 variables and print Variable Addresses and values by using pointer.
```c++
#include <iostream>

using namespace std;

int main() {
    // Declare variables
    int a = 10, b = 20, c = 30;
    double x = 3.14, y = 2.718;

    // Declare pointers
    int *ptr_a = &a;
    int *ptr_b = &b;
    int *ptr_c = &c;
    double *ptr_x = &x;
    double *ptr_y = &y;

    // Print addresses and values of variables using pointers
    cout << "Variable a - Address: " << ptr_a << ", Value: " << *ptr_a << endl;
    cout << "Variable b - Address: " << ptr_b << ", Value: " << *ptr_b << endl;
    cout << "Variable c - Address: " << ptr_c << ", Value: " << *ptr_c << endl;
    cout << "Variable x - Address: " << ptr_x << ", Value: " << *ptr_x << endl;
    cout << "Variable y - Address: " << ptr_y << ", Value: " << *ptr_y << endl;

    return 0;
}
```
### Output :
    Variable a - Address: 0x7ffebdde36d4, Value: 10
    Variable b - Address: 0x7ffebdde36d8, Value: 20
    Variable c - Address: 0x7ffebdde36dc, Value: 30
    Variable x - Address: 0x7ffebdde36e0, Value: 3.14
    Variable y - Address: 0x7ffebdde36e8, Value: 2.718


## 4. Take a variable and print Variable Addresses and values by using pointer and the change the value by using pointer.

```c++
#include <iostream>

using namespace std;

int main() {
    int myVariable = 42;
    int *ptr = &myVariable;
    cout << "Original - Address: " << ptr << ", Value: " << *ptr << endl;
    *ptr = 99;
    cout << "Updated  - Address: " << ptr << ", Value: " << *ptr << endl;

    return 0;
}
```
### Output :
    Original - Address: 0x7ffda8ffcf1c, Value: 42
    Updated  - Address: 0x7ffda8ffcf1c, Value: 99