# IP Lab Task 5 ; Md Rijoan Maruf (23-53347-3)
## 1. Enter the marks of 5 students in Chemistry, Mathematics and Physics (each out of 100) using a structure named Marks having elements roll no., name, chemistry marks, phy_maths and phy_marks and then display the percentage of each student.

```c++
#include <iostream>
#include <cstring>
using namespace std;

struct Marks {
    int roll;
    string name;
    float chem_marks;
    float maths_marks;
    float phy_marks;
};

int main() {
    Marks students[5];

    for (int i = 0; i < 5; ++i) {
        cout << "Enter details for student " << i + 1 << ":" << endl;
        cout << "Roll No.: ";
        cin >> students[i].roll;
        cout << "Name: ";
        cin >> students[i].name;
        cout << "Chemistry Marks (out of 100): ";
        cin >> students[i].chem_marks;
        cout << "Math Marks (out of 100): ";
        cin >> students[i].maths_marks;
        cout << "Physics Marks (out of 100): ";
        cin >> students[i].phy_marks;
        cout << endl;
    }

    cout << "Displaying percentages of each student:" << endl;
    for (int i = 0; i < 5; ++i) {
        float totalMarks = students[i].chem_marks + students[i].maths_marks + students[i].phy_marks;
        float percentage = (totalMarks / 300) * 100;

        cout << "Student " << i + 1 << " - " << students[i].name << ": " << percentage << "%" << endl;
    }

    return 0;
}
```
### Output :
    Enter details for student 1:
    Roll No.: 45564
    Name: Saif
    Chemistry Marks (out of 100): 77
    Math Marks (out of 100): 88
    Physics Marks (out of 100): 99

    Enter details for student 2:
    Roll No.: 34566
    Name: Rijoan
    Chemistry Marks (out of 100): 76
    Math Marks (out of 100): 86
    Physics Marks (out of 100): 78

    Enter details for student 3:
    Roll No.: 55674
    Name: Reyad
    Chemistry Marks (out of 100): 77
    Math Marks (out of 100): 89
    Physics Marks (out of 100): 91

    Enter details for student 4:
    Roll No.: 454665
    Name: Rudorjit
    Chemistry Marks (out of 100): 77
    Math Marks (out of 100): 68
    Physics Marks (out of 100): 94

    Enter details for student 5:
    Roll No.: 345454
    Name: Fahim
    Chemistry Marks (out of 100): 74
    Math Marks (out of 100): 89
    Physics Marks (out of 100): 49

    Displaying percentages of each student:
    Student 1 - Saif: 88%
    Student 2 - Rijoan: 80%
    Student 3 - Reyad: 85.6667%
    Student 4 - Rudorjit: 79.6667%
    Student 5 - Fahim: 70.6667%

## 2. Write a structure to store the roll no., name, age (between 11 to 14) and address of students (more than 10). Store the information of the students
**1. Write a fiunction to print the names of all the students having age 14.**

**2. Write another function to print the names of all the students having even roll no.**

**3. Write another function to display the details of the student whose roll no is given (ie. roll no. entered by the user)**


```c++
#include <iostream>
#include <string>
using namespace std;

struct Student {
    int rollNo;
    string name;
    int age;
    string address;
};

void age14(Student student[3]) {
    cout << "Names of students aged 14:\n";
    for (int i = 0; i < 3; i++) {
        if (student[i].age == 14) {
            cout << student[i].name << endl;
        }
    }
}

void evenRollNumbers(Student student[3]) {
    cout << "Names of students with even roll numbers:\n";
    for (int i = 0; i < 3; i++) {
        if (student[i].rollNo % 2 == 0) {
            cout << student[i].name << endl;
        }
    }
}

void displayDetails(Student student[3], int rollNumber) {
    cout << "Details of student with roll number " << rollNumber << ":\n";
    for (int i = 0; i < 3; i++) {
        if (student[i].rollNo == rollNumber) {
            cout << "Roll Number: " << student[i].rollNo << endl;
            cout << "Name: " << student[i].name << endl;
            cout << "Age: " << student[i].age << endl;
            cout << "Address: " << student[i].address << endl;
            return;
        }
    }
    cout << "Student with roll number " << rollNumber << " not found." << endl;
}

int main() {
    Student stu[3];
    for (int i = 0; i < 3; i++) {
        cout << "Enter roll number of student " << i + 1 << ": ";
        cin >> stu[i].rollNo;
        cout << "Enter name of student " << i + 1 << ": ";
        cin.ignore();
        getline(cin, stu[i].name);
        cout << "Enter age of student " << i + 1 << ": ";
        cin >> stu[i].age;
        cout << "Enter address of student " << i + 1 << ": ";
        cin.ignore();
        getline(cin, stu[i].address);
        cout << endl;
    }

    age14(stu);
    evenRollNumbers(stu);

    int rollToFind;
    cout << endl;
    cout << "Enter roll number to display details: ";
    cin >> rollToFind;
    displayDetails(stu, rollToFind);

    return 0;
}
```

### Output :
    Enter roll number of student 1: 11111
    Enter name of student 1: Rijoan Maruf
    Enter age of student 1: 14
    Enter address of student 1: F Block

    Enter roll number of student 2: 2222
    Enter name of student 2: Dey Rudrojit
    Enter age of student 2: 13
    Enter address of student 2: C Block

    Enter roll number of student 3: 3333
    Enter name of student 3: Shahariya alam
    Enter age of student 3: 15
    Enter address of student 3: Kuril 

    Names of students aged 14:
    Rijoan Maruf
    Names of students with even roll numbers:
    Dey Rudrojit

    Enter roll number to display details: 14
    Roll number : 11111
    Name : Rijoan Maruf
    Age : 14
    Address : F Block

