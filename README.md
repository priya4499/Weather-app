Name: PRIYADHARSHINI S
College: ERODE SENGUNTHAR ENGINEERING COLLEGE 

#include <iostream>

using namespace std;


class Weather {
private:
    string city;
    double temperature;
    double humidity;

public:
    Weather(string cityName, double temp, double hum) {
        city = cityName;
        temperature = temp;
        humidity = hum;
    }

    void displayWeather() {
        cout << "Weather Condition in " << city << endl;
        cout << "Temperature: " << temperature << "°C" << endl;
        cout << "Humidity: " << humidity << "%" << endl;
    }

    void updateWeather(double newTemp, double newHum) {
        temperature = newTemp;
        humidity = newHum;
    }
};

int main() {
    Weather london("London", 23.5, 70.0);
    london.displayWeather();

    cout << "\nUpdating weather...\n" << endl;

    london.updateWeather(25.0, 65.0);
    london.displayWeather();

    return 0;
}
