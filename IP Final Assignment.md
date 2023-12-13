# IP Final Assignment





## Question 1: Define all the known string functions with example.

* **strcmp** - Compares two strings and returns an integer value:

strcmp compares two strings lexicographically. It returns an integer value less than, equal to, or greater than zero if the first string is found to be less than, equal to, or greater than the second string, respectively.

* **strcpy** - Copies one string to another:

strcpy copies the contents of one string to another, including the null-terminating character.


* **strlen** - Determines the length of a string:

strlen calculates and returns the length of a string excluding the null-terminating character.


* **strchr** - Finds the first occurrence of a character in a string:

strchr searches for the first occurrence of a specified character in a string and returns a pointer to the location if found, or null if the character is not found.


* **strstr** - Finds the first occurrence of a substring in a string:

strstr searches for the first occurrence of a specified substring within a string and returns a pointer to the location if found, or null if the substring is not found.


### Example :
```c++
#include <iostream>
#include <cstring>
using namespace std;

int main() {
    // strcmp example
    const char *str1 = "hello";
    const char *str2 = "world";
    int result = strcmp(str1, str2);
    cout << "strcmp result: " << result << endl;

    // strcpy example
    char dest[20];
    const char *src = "Copying this string";
    strcpy(dest, src);
    cout << "strcpy result: " << dest << endl;

    // strlen example
    const char *lengthTest = "Length test";
    cout << "strlen result: " << strlen(lengthTest) << endl;

    // strchr example
    const char *str = "Find character 'e'";
    char ch = 'e';
    const char *found = strchr(str, ch);
    if (found != nullptr) {
        cout << "strchr result: Character '" << ch << "' found at position: " << (found - str) << endl;
    } else {
        cout << "strchr result: Character not found" << endl;
    }

    // strstr example
    const char *mainStr = "This is a test string";
    const char *subStr = "test";
    const char *subFound = strstr(mainStr, subStr);
    if (subFound != nullptr) {
        cout << "strstr result: Substring '" << subStr << "' found at position: " << (subFound - mainStr) << endl;
    } else {
        cout << "strstr result: Substring not found" << endl;
    }

    return 0;
}
```

### Output :
    strcmp result: -15
    strcpy result: Copying this string
    strlen result: 11
    strchr result: Character 'e' found at position: 2
    strstr result: Substring 'test' found at position: 10



## Question 2 : Define 2D array(include example)

A 2D array in C++ is a matrix-like structure containing elements arranged in rows and columns. It is declared using square brackets `[][]` to represent multiple dimensions, such as `int arr[3][4]` for a 3x4 array.
### Example :
```c++
#include <iostream>
using namespace std;

int main() {
    int arr[3][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12}
    };

    cout << "Elements of the 2D array:" << endl;
    for (int i = 0; i < 3; ++i) {
        for (int j = 0; j < 4; ++j) {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```
### Output :
    Elements of the 2D array:
    1 2 3 4 
    5 6 7 8 
    9 10 11 12 

## Question 3 : Define pointer with its mechanism. 
A pointer in C++ is a variable that holds the memory address of another variable. It allows indirect access to that variable's value.
### Example :
```c++
#include <iostream>
using namespace std;

int main() {
    int x = 10; 
    int *ptr = &x; 

    cout << "Value of x: " << x << endl;
    cout << "Address of x: " << &x << endl;
    cout << "Value stored in ptr: " << *ptr << endl;

    return 0;
}
```

### Output :
    Value of x: 10
    Address of x: 0x7f5a62b6c 
    Value stored in ptr: 10

## Question 4:
**Write a c++ program containing following functions .**
1. Swap function which take two values as parameter and
swaps them, simultaneously shows the swapped values

2. A function to print the maximum number respectively
among three numbers entered by user.

3. A function to print the minimum number respectively
among three numbers entered by user.

4. A function to print all the prime numbers till a number given
as a parameter.

### Code :
```c++
#include <iostream>
using namespace std;

void swapValues(int &a, int &b) {
    cout << "Before swapping: a = " << a << ", b = " << b << endl;
    int temp = a;
    a = b;
    b = temp;
    cout << "After swapping: a = " << a << ", b = " << b << endl;
}

void findMax(int num1, int num2, int num3) {
    int maxNum;
    if (num1 > num2) {
        if (num1 > num3) {
            maxNum = num1;
        } else {
            maxNum = num3;
        }
    } else {
        if (num2 > num3) {
            maxNum = num2;
        } else {
            maxNum = num3;
        }
    }
    cout << "Maximum number: " << maxNum << endl;
}

void findMin(int num1, int num2, int num3) {
    int minNum;
    if (num1 < num2) {
        if (num1 < num3) {
            minNum = num1;
        } else {
            minNum = num3;
        }
    } else {
        if (num2 < num3) {
            minNum = num2;
        } else {
            minNum = num3;
        }
    }
    cout << "Minimum number: " << minNum << endl;
}

bool isPrime(int num) {
    if (num <= 1) {
        return false;
    } else {
        for (int i = 2; i * i <= num; ++i) {
            if (num % i == 0) {
                return false;
            }
        }
        return true;
    }
}

void printPrimes(int limit) {
    cout << "Prime numbers till " << limit << " are: ";
    for (int i = 2; i <= limit; ++i) {
        if (isPrime(i)) {
            cout << i << " ";
        }
    }
    cout << endl;
}

int main() {
    int a, b, c;
    cout << "Enter three numbers: ";
    cin >> a >> b >> c;

    swapValues(a, b);
    findMax(a, b, c);
    findMin(a, b, c);

    int limit;
    cout << "Enter a number to find prime numbers till that limit: ";
    cin >> limit;
    printPrimes(limit);

    return 0;
}
```

### Output :
    Enter three numbers: 8 15 5
    Before swapping: a = 8, b = 15
    After swapping: a = 15, b = 8
    Maximum number: 15
    Minimum number: 5
    Enter a number to find prime numbers till that limit: 20
    Prime numbers till 20 are: 2 3 5 7 11 13 17 19

