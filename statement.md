# 
```C++ runnable
#include<iostream>


const double DELTA = 0.00001;
double sqrtdemo(double n)
{
    double low = 1;
    double high = n;
    double middle = 0;
    while ((high - low) > DELTA)
    {
        middle = low + (high - low)/2;
        double tmp = middle*middle;
        if ( tmp - n > DELTA) {
            high = middle;
        }
        else {
            low = middle;
        }
    }
    return middle;
}

int main()
{
    std::cout << sqrtdemo(2.0) << std::endl;
}        
