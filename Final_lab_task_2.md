# Final Lab Task 2 (Function)

## 1. Write a C++ program to calculate area and circumference of circle using function.
```c++
#include <iostream>
using namespace std;

const double PI = 3.14159;

// Calculate the area of a circle
double calculateArea(double radius) {
    return PI * radius * radius;
}

// Calculate the circumference of a circle
double calculateCircumference(double radius) {
    return 2 * PI * radius;
}

int main() {
    double radius;
    cout << "Enter the radius of the circle: ";
    cin >> radius;

    // Calculate area and circumference using functions
    double area = calculateArea(radius);
    double circumference = calculateCircumference(radius);

    cout << "Area of the circle: " << area << endl;
    cout << "Circumference of the circle: " << circumference << endl;

    return 0;
}
```

### Output :
    Enter the radius of the circle: 5
    Area of the circle: 78.5397
    Circumference of the circle: 31.4159

## 2. Write a C++ program to delete all the vowels from the string using function.
```c++
#include <iostream>

using namespace std;

void removeVowels(string &str) {
    for (int i = 0; i < str.length(); i++) {
        if (str[i] == 'a' || str[i] == 'e' || str[i] == 'i' || str[i] == 'o' || str[i] == 'u' ||
            str[i] == 'A' || str[i] == 'E' || str[i] == 'I' || str[i] == 'O' || str[i] == 'U') {
            str.erase(i, 1);
            i--;
        }
    }
}

int main() {
    string str;
    cout << "Enter the string: ";
    cin >> str;

    removeVowels(str);

    cout << "String without vowels: " << str << endl;

    return 0;
}
```
### Output :
    Enter the string: rijoan
    String without vowels: rjn

## 3. Write a C++ program to display the addition of two numbers using function.
```c++
#include <iostream>

using namespace std;

int addition(int num1, int num2) {
  int sum = num1 + num2;
  return sum;
}

int main() {
  int x, y, sum;
  cout << "Enter two numbers: ";
  cin >> x >> y;

  sum = addition(x, y);

  cout << x << " + " << y << " = " << sum << endl;

  return 0;
}
```

### Output :
    Enter two numbers: 10 20
    10 + 20 = 30