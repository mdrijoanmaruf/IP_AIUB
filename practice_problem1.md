# Practice Problem 1
### 1. Write a program to print from 1 to 10.

```c++
#include <iostream>

using namespace std;

int main(){
    for(int i = 1; i <= 10; i++){
        cout << i << endl;
    }
    return 0;
}
```

### 2. Write a program to calculate the sum of first 10 number.
```c++
#include <iostream>

using namespace std;

int main(){
    int sum = 0;
    for(int i = 1; i <= 10; i++){
        sum = sum + i;
    }
    cout << "Sum is : " << sum << endl;
    return 0;
}
```

### 3. Two numbers are entered through the keyboard. Write a program to find the value of one number raised to the power of another.
```c++
#include <iostream>

using namespace std;

int main() {
    double number1, result = 1;
    int number2;

    cout << "Enter the number1 number: ";
    cin >> number1;

    cout << "Enter the number2: ";
    cin >> number2;

    if (number2 >= 0) {
        for (int i = 1; i <= number2; i++) {
            result *= number1;
        }
    } 
    else {
        for (int i = 1; i <= -number2; i++) {
            result /= number1;
        }
    }

    cout << number1 << " Raised to the power of " << number2 << " is: " << result << endl;
    return 0;
}
```

### 4. A person wants to calculate the total amount of money they have saved in a year. Write a program that asks the user to input the amount of money they save each month, and then calculates the total amount of money saved in a year.
```c++
#include <iostream>

using namespace std;

int main() {
    double monthlySavings;
    double totalSavings = 0.0;

    for (int month = 1; month <= 12; month++) {
        cout << "Enter the amount saved in month " << month << ": $";
        cin >> monthlySavings;
        totalSavings += monthlySavings;
    }

    cout << "Total savings in a year: " << totalSavings << endl;

    return 0;
}
```

### 5. Write a program that calculates the average distance from the Sun of all the planets in the solar system. The program should ask the user to enter the distance from the Sun for each planet, and then use a loop to calculate the average distance.
```c++
#include <iostream>
#include <string>

using namespace std;

int main() {
    int planet;
    cout << "How many plantes you want to count ? : ";
    cin >> planet; 

    double totalDistance = 0;

    for (int i = 0; i < planet; i++) {
        double distance;
        cout << "Enter the distance for Planate " << i+1 << " :";
        cin >> distance;
        totalDistance += distance;
    }

    double avgDistence = totalDistance / planet;
    cout << "The average distance of all planets is: " << avgDistence  << endl;
    return 0;
}
```

### 6. Write a program that calculates the sum of the first n terms of the series 1 - 1/2 + 1/3 - ... + (-1)^n/n. The program should ask the user to enter the value of n, and then use a loop to calculate the sum.
```c++
#include <iostream>

using namespace std;

int main() {
    int n;
    double sum = 0;

    cout << "Enter the value of n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        double term = 1.0 / i;
        if (i % 2 == 0) {
            sum -= term;  // for even values of i
        } else {
            sum += term;  // for odd values of i
        }
    }

    cout << "The sum of the first " << n << " terms of the series is: " << sum << endl;
    return 0;
}
```

### 7. Write a program that calculates the sum of the first n terms of the Fibonacci series (1, 1, 2, 3, 5, 8, ...). The program should ask the user to enter the value of n, and then use a loop to calculate the sum.
```c++
#include <iostream>

using namespace std;

int main() {
    int n;
    int first = 1, last = 1, next;
    int sum = 0;

    cout << "Enter the value of n: ";
    cin >> n;

    if (n >= 1) {
        sum += first;  
    }

    if (n >= 2) {
        sum += last;  
    }

    for (int i = 3; i <= n; i++) {
        next = first + last;
        sum += next;
        first = last;
        last = next;
    }

    cout << "The sum of the first " << n << " terms of the Fibonacci series is: " << sum << endl;

    return 0;
}
```

### 8. Write a program that calculates the sum of all the even numbers between 1 and a given number. For example, if the user inputs the number 10, the program should print out 30 (which is the sum of 2+4+6+8+10).
```c++
#include <iostream>

using namespace std;

int main() {
    int n;
    int sum = 0;

    cout << "Enter a number: ";
    cin >> n;

    for (int i = 2; i <= n; i += 2) {
        sum += i;
    }

    cout << "The sum of even numbers between 1 and " << n << " is: " << sum << endl;

    return 0;
}
```

### 9. Write a program that calculates the sum of the squares of all the odd numbers between 1 and a given number. For example, if the user inputs the number 10, the program should print out 165 (which is the sum of 1+9+25+49+81).
```c++
#include <iostream>

using namespace std;

int main() {
    int n;
    int sum = 0;

    cout << "Enter a number: ";
    cin >> n;

    for (int i = 1; i <= n; i += 2) {
        sum += i * i;
    }

    cout << "The sum of the squares of odd numbers between 1 and " << n << " is: " << sum << endl;
    return 0;
}
```

### 10. Write a program that calculates the sum of all the numbers divisible by 3 between 1 and a given number. For example, if the user inputs the number 9, the program should print out 18 (which is the sum of 3+6+9).
```c++
#include <iostream>

using namespace std;

int main() {
    int n;
    int sum = 0;

    cout << "Enter a number: ";
    cin >> n;

    for (int i = 3; i <= n; i += 3) {
        sum += i;
    }

    cout << "The sum of numbers divisible by 3 between 1 and " << n << " is: " << sum << endl;
    return 0;
}
```

### 11. A weather station wants to calculate the average temperature and humidity over a certain period (5 days). Write a program that asks the user to input the temperature and humidity readings for five days and calculate rates for the average temperature and humidity.
```c++
#include <iostream>

using namespace std;

int main() {
    int days = 5;  
    double temp, hum;
    double total_temp = 0, total_hum = 0;

    for (int day = 1; day <= days; day++) {
        cout << "Enter the temp for Day " << day << " : ";
        cin >> temp;
        total_temp += temp;

        cout << "Enter the hum for Day " << day << " : ";
        cin >> hum;
        cout << endl;
        total_hum += hum;
    }

    double avg_temp = total_temp / days;
    double avg_hum = total_hum / days;

    cout << "Average temp for " << days << " days: " << avg_temp << endl;
    cout << "Average Humidity over " << days << " days: " << avg_hum << endl;

    return 0;
}
```

### 12. Write a program that asks the user to enter the name and diameter of each planet in the solar system and print them in the Command Prompt. The program should then use a loop to print out the name and diameter of each planet.
```c++
#include <iostream>
#include <string>

using namespace std;

int main() {
    int planet;
    cout << "How many planet you want to count ? : ";
    cin >> planet;

    string name[planet];
    double diameter[planet];

    for (int i = 0; i < planet; i++) {
        cout << "Enter the name of planet " << (i + 1) << ": ";
        cin.ignore(); 
        getline(cin, name[i]);

        cout << "Enter the diameter of planet " << name[i] << " : ";
        cin >> diameter[i];
    }

    cout << "List of planets and their diameters:\n";
    for (int i = 0; i < planet; i++) {
        cout << "Planet Name: " << name[i] << ", Diameter: " << diameter[i] << endl;
    }

    return 0;
}
```

### 13. Write a program that calculates the total mass of the solar system. The program should ask the user to enter the mass of each planet, and then use a loop to calculate the total mass.
```c++
#include <iostream>
#include <string>

using namespace std;

int main() {
    const int planet = 8;
    string planetNames[planet] = {"Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"};
    double planetMasses[planet];

    double totalMass = 0;

    for (int i = 0; i < planet; i++) {
        cout << "Enter the mass of " << planetNames[i] << " : ";
        cin >> planetMasses[i];
        totalMass += planetMasses[i];
    }

    cout << "Total mass of the solar system is approximately : " << totalMass << endl;

    return 0;
}
```

### 14. Write a program that calculates the average density of the planets in the solar system. The program should ask the user to enter the mass and diameter of each planet, and then use a loop to calculate the average density (mass divided by volume). 
```c++
#include <iostream>
#include <string>
#include <cmath>

using namespace std;

int main() {
    int planate = 8;
    float pi = 3.1416;
    string name[planate] = {"Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"};
    double mass[planate];
    double diameter[planate];

    double total_dens = 0;

    for (int i = 0; i < planate; i++) {
        cout << "Enter the mass of " << name[i] << " : ";
        cin >> mass[i];

        cout << "Enter the diameter of " << name[i] << " : ";
        cin >> diameter[i];

        // V = (4/3) * π * (r^3)
        double radius = diameter[i] / 2.0;
        double volume = (4.0 / 3.0) * pi * pow(radius, 3); 

        double density = mass[i] / volume;
        total_dens += density;
    }

    double averageDensity = total_dens / planate;

    cout << "Average density of the planets in the solar system : " << averageDensity  << endl;

    return 0;
}
```

### 15. Write a program that keeps track of the number of copies of each comic book in a collection. The program should ask the user to enter the name and quantity of each comic book, and then use a loop to update the count for each comic book.
```c++
#include <iostream>
#include <string>

using namespace std;

int main() {
    int maxComics;  
    cout << "Enter Comics number : ";
    cin >> maxComics;

    string comicNames[maxComics];
    int comicQuantities[maxComics];
    int numComics = 0;  
    int i = 0;

    while (i < maxComics) {
        cout << "Enter the name of the comic book : ";
        cin >> comicNames[i];

        cout << "Enter the quantity of copies: ";
        cin >> comicQuantities[i];
        i++;
    }

    cout << "\nComic Collection:\n";
    for (int i = 0; i < maxComics; i++) {
        cout << "Comic Book: " << comicNames[i] << ", Quantity: " << comicQuantities[i] << endl;
    }

    return 0;
}
```

### 16. Write a program that calculates the sum of the first n terms of the series 1 + 2 + 3 + ... + n. The program should ask the user to enter the value of n, and then use a loop to calculate the sum.
```c++
#include <iostream>

using namespace std;

int main() {
    int n;
    int sum = 0;

    cout << "Enter the value of n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        sum += i;
    }

    cout << "The sum of the first " << n << " terms is: " << sum << endl;
    return 0;
}
```

### 17. Write a program that calculates the sum of the first n terms of the series 1 + 1/2 + 1/3 + ... + 1/n. The program should ask the user to enter the value of n, and then use a loop to calculate the sum.
```c++
#include <iostream>

using namespace std;

int main() {
    int n;
    double sum = 0;

    cout << "Enter the value of n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        sum += 1.0 / i;  
    }

    cout << "The sum of the first " << n << " terms is: " << sum << endl;
    return 0;
}
```