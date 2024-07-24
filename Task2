#include <iostream>
#include <string>
#include <cctype>

using namespace std;

double celsiusToFahrenheit(double celsius) {
    return (celsius * 9.0/5.0) + 32.0;
}

double celsiusToKelvin(double celsius) {
    return celsius + 273.15;
}

double fahrenheitToCelsius(double fahrenheit) {
    return (fahrenheit - 32.0) * 5.0/9.0;
}

double fahrenheitToKelvin(double fahrenheit) {
    return (fahrenheit - 32.0) * 5.0/9.0 + 273.15;
}

double kelvinToCelsius(double kelvin) {
    return kelvin - 273.15;
}

double kelvinToFahrenheit(double kelvin) {
    return (kelvin - 273.15) * 9.0/5.0 + 32.0;
}

double convertTemperature(double temp, char fromScale, char toScale) {
    fromScale = toupper(fromScale);
    toScale = toupper(toScale);
    
    if (fromScale == 'C') {
        if (toScale == 'F') {
            return celsiusToFahrenheit(temp);
        } else if (toScale == 'K') {
            return celsiusToKelvin(temp);
        }
    } else if (fromScale == 'F') {
        if (toScale == 'C') {
            return fahrenheitToCelsius(temp);
        } else if (toScale == 'K') {
            return fahrenheitToKelvin(temp);
        }
    } else if (fromScale == 'K') {
        if (toScale == 'C') {
            return kelvinToCelsius(temp);
        } else if (toScale == 'F') {
            return kelvinToFahrenheit(temp);
        }
    }
    return -1; // Return -1 if conversion is not possible
}

int main() {
    double temp;
    char fromScale, toScale;

    cout << "Enter the temperature: ";
    cin >> temp;
    cout << "Enter the scale of the temperature (C, F, K): ";
    cin >> fromScale;
    cout << "Enter the scale to convert to (C, F, K): ";
    cin >> toScale;

    if (toupper(fromScale) != 'C' && toupper(fromScale) != 'F' && toupper(fromScale) != 'K' || 
        toupper(toScale) != 'C' && toupper(toScale) != 'F' && toupper(toScale) != 'K') {
        cout << "Invalid scale input. Please enter C, F, or K." << endl;
        return 1;
    }

    double convertedTemp = convertTemperature(temp, fromScale, toScale);

    if (convertedTemp != -1) {
        cout << temp << "°" << fromScale << " is " << convertedTemp << "°" << toScale << endl;
    } else {
        cout << "Conversion not possible. Check the input scales." << endl;
    }

    return 0;
}
