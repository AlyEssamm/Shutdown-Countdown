# Shutdown-Countdown
in this app you place a certain amount of time and after that time ends your computer will automatically shutdown for you

thats it... 

heres the source code:
//in c++

#include <iostream>
#include <Windows.h>
using namespace std;

int main()
{
    cout << "1 hour = 3600  2 hours = 7200   \n3 hours 10800  4 hours = 14400\n";
    cout << "Enter the time you want (Seconds):";
    int counter{};
    cin >> counter;
    Sleep(1000);
    while (counter >= 1)
    {
        cout << "\rTime remaining: " << counter << flush;
        Sleep(1000);
        counter--;
    }
    if (counter == 0)
        system("C:\\WINDOWS\\System32\\shutdown -s");
}
