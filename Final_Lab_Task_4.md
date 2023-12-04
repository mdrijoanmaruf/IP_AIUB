# Object Oriented Programming Basic Problem
```c++
#include <iostream>
using namespace std;

class Mobile
{
private:
    int imei;

public:
    string model;
    string screen;

    // Constructor
    Mobile()
    {
        imei = 0;
    }

    // Parameterized Constructor
    Mobile(string model, string screen, int imei)
    {
        this->model = model;
        this->screen = screen;
        this->imei = imei;
    }

    // Destructor
    ~Mobile()
    {
        cout << "Mobile object destroyed" << endl;
    }

    void SetModel(string model)
    {
        this->model = model;
    }

    string GetModel()
    {
        return this->model;
    }

    void SetScreen(string screen)
    {
        this->screen = screen;
    }

    string GetScreen()
    {
        return this->screen;
    }

    void SetImeiNo(int imei)
    {
        this->imei = imei;
    }

    int GetImeiNo()
    {
        return this->imei;
    }
};

class Samsung
{
public:
    string model;
    string screen;
    int imei;
    string version;

    Samsung(string model, string screen, int imei, string version)
    {
        this->model = model;
        this->screen = screen;
        this->imei = imei;
        this->version = version;
    }

    string GetModel() {
         return this->model; 
    }
    string GetScreen() {
         return this->screen; 
    }
    int GetImeiNo() {
         return this->imei; 
    }
    string GetOsVersion() {
         return this->version; 
    }
};

class iPhone
{
public:
    string model;
    string screen;
    int imei;
    string chip;

    iPhone(string model, string screen, int imei, string chip)
    {
        this->model = model;
        this->screen = screen;
        this->imei = imei;
        this->chip = chip;
    }

    string GetModel() {
         return this->model; 
    }
    string GetScreen() {
         return this->screen; 
    }
    int GetImeiNo() {
         return this->imei; 
    }
    string GetChipType() {
         return this->chip; 
    }
};

class Nokia
{
public:
    string model;
    string screen;
    int imei;
    string battery;

    Nokia(string model, string screen, int imei, string battery)
    {
        this->model = model;
        this->screen = screen;
        this->imei = imei;
        this->battery = battery;
    }

    string GetModel() {
         return this->model; 
    }
    string GetScreen() {
         return this->screen; 
    }
    int GetImeiNo() {
         return this->imei; 
    }
    string GetBatteryCapacity() {
         return this->battery; 
    }
};

int main()
{
    Samsung s1("Galaxy S23 Ultra", "AMOLED", 1234567890, "13");
    iPhone i1("iPhone 15 Pro", "OLED", 9876543210, "A16");
    Nokia n1("AAA", "IPS LCD", 9876543210, "5050 mAh");

    cout << "Samsung S23" << endl;
    cout << "Model: " << s1.GetModel() << endl;
    cout << "Screen: " << s1.GetScreen() << endl;
    cout << "IMEI No: " << s1.GetImeiNo() << endl;
    cout << "OS Version: " << s1.GetOsVersion() << endl;
    cout << endl;

    cout << "iPhone 15 Pro" << endl;
    cout << "Model: " << i1.GetModel() << endl;
    cout << "Screen: " << i1.GetScreen() << endl;
    cout << "IMEI No: " << i1.GetImeiNo() << endl;
    cout << "Chip Type: " << i1.GetChipType() << endl;
    cout << endl;

    cout << "Nokia AAA" << endl;
    cout << "Model: " << n1.GetModel() << endl;
    cout << "Screen: " << n1.GetScreen() << endl;
    cout << "IMEI No: " << n1.GetImeiNo() << endl;
    cout << "Battery Capacity: " << n1.GetBatteryCapacity() << endl;
    cout << endl;

    return 0;
}
```

## Output :
    Samsung S23
    Model: Galaxy S23 Ultra
    Screen: AMOLED
    IMEI No: 1234567890
    OS Version: 13

    iPhone 15 Pro
    Model: iPhone 15 Pro
    Screen: OLED
    IMEI No: 1286608618
    Chip Type: A16

    Nokia AAA
    Model: AAA
    Screen: IPS LCD
    IMEI No: 1286608618
    Battery Capacity: 5050 mAh
