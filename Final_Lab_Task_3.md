# Final Lab Task 3

## 1. Develop a program that has two 2D matrices of same size. Later, the program displays the rows, columns of each array as well as performs matrix addition,subtraction, and multiplication between the matrices. Finally, the program prints all the results.
```c++
#include <iostream>

using namespace std;

int main() {
  int m1[3][3], m2[3][3], sum[3][3], diff[3][3], prod[3][3];

  cout << "Enter the first matrix: " << endl;
  for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
      cin >> m1[i][j];
    }
  }

  cout << "Enter the second matrix: " << endl;
  for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
      cin >> m2[i][j];
    }
  }

  for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
      sum[i][j] = m1[i][j] + m2[i][j];
      diff[i][j] = m1[i][j] - m2[i][j];
      prod[i][j] = m1[i][j] * m2[i][j];
    }
  }

  cout << "Sum of the matrices: " << endl;
  for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
      cout << sum[i][j] << " ";
    }
    cout << endl;
  }

  cout << "Difference of the matrices: " << endl;
  for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
      cout << diff[i][j] << " ";
    }
    cout << endl;
  }

  cout << "Product of the matrices: " << endl;
  for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
      cout << prod[i][j] << " ";
    }
    cout << endl;
  }

  return 0;
}
```
### Output :
    Enter the first matrix:
    1 2 3
    4 5 6
    7 8 9
    Enter the second matrix:
    10 11 12
    13 14 15
    16 17 18

    Sum of the matrices:
    11 13 15
    17 19 21
    23 25 27

    Difference of the matrices:
    -9 -9 -9
    -9 -9 -9
    -9 -9 -9

    Product of the matrices:
    70 84 98
    146 174 202
    222 264 306


## 2. Develop a program that stores five countries' names using a single 2D array and prints the names at the end.
```c++
#include <iostream>

using namespace std;

int main() {
  string countries[5];

  cout << "Enter five countries: " << endl;
  for (int i = 0; i < 5; i++) {
    cin >> countries[i];
  }
  cout << "The five countries are: " << endl;
  for (int i = 0; i < 5; i++) {
    cout << countries[i] << endl;
  }

  return 0;
}
```

### Output :
    Enter five countries:
    Bangladesh
    India
    Pakistan
    Nepal
    China

    The five countries are:
    Bangladesh
    India
    Pakistan
    Nepal
    China

## 3. Develop a program that has a 2D array that can hold floating point numbers. The 2D array has 2 rows and four columns. The program finds the largest element from the first row, the smallest element from the second row, multiplies them and displays the largest element, smallest element as well as the multiplied result.
￼
```c++
#include <iostream>
using namespace std;

int main() {
  float array[2][4] = {{12.34, 56.78, 90.12, 34.56},
                         {23.45, 67.89, 10.12, 45.67}};

  float large = array[0][0];
  for (int i = 1; i < 4; i++) {
    if (array[0][i] > large) {
      large = array[0][i];
    }
  }

  float small = array[1][0];
  for (int i = 1; i < 4; i++) {
    if (array[1][i] < small) {
      small = array[1][i];
    }
  }

  float product = large * small;
  cout << "Largest element in the first row: " << large << endl;
  cout << "Smallest element in the second row: " << small << endl;
  cout << "Product of largest and smallest elements: " << product << endl;

  return 0;
}
#include <iostream>
using namespace std;

int main() {
  float array[2][4] = {{12.34, 56.78, 90.12, 34.56},
                         {23.45, 67.89, 10.12, 45.67}};

  float large = array[0][0];
  for (int i = 1; i < 4; i++) {
    if (array[0][i] > large) {
      large = array[0][i];
    }
  }

  float small = array[1][0];
  for (int i = 1; i < 4; i++) {
    if (array[1][i] < small) {
      small = array[1][i];
    }
  }

  float product = large * small;
  cout << "Largest element in the first row: " << large << endl;
  cout << "Smallest element in the second row: " << small << endl;
  cout << "Product of largest and smallest elements: " << product << endl;

  return 0;
}
```

### Output :
    Largest element in the first row: 90.12
    Smallest element in the second row: 10.12
    Product of largest and smallest elements: 912.014

## 4. Develop a program that has a 2D array that stores floating point numbers given by user. Later, the program takes a number as input and searches the number whether it is present or not present in the array.

```c++
#include <iostream>
using namespace std;

int main() {
  int rows, columns;
  cout << "Enter the number of rows: ";
  cin >> rows;

  cout << "Enter the number of columns: ";
  cin >> columns;

  float array[rows][columns];

  for (int i = 0; i < rows; i++) {
    for (int j = 0; j < columns; j++) {
      cout << "Enter element [" << i << ", " << j << "]: ";
      cin >> array[i][j];
    }
  }

  float searchNumber;
  cout << "Enter the number to search: ";
  cin >> searchNumber;

  bool found = false;

  for (int i = 0; i < rows; i++) {
    for (int j = 0; j < columns; j++) {
      if (array[i][j] == searchNumber) {
        found = true;
        break; 
      }
    }
  }

  if (found) {
    cout << "The number " << searchNumber << " is present in the array." << endl;
  } else {
    cout << "The number " << searchNumber << " is not present in the array." << endl;
  }

  return 0;
}
```
### Output :
    Enter the number of rows: 2
    Enter the number of columns: 3

    Enter element [0, 0]: 12.34
    Enter element [0, 1]: 56.78
    Enter element [0, 2]: 90.12

    Enter element [1, 0]: 23.45
    Enter element [1, 1]: 67.89
    Enter element [1, 2]: 10.12

    Enter the number to search: 12.34
    The number 12.34 is present in the array.