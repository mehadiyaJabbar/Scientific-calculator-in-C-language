#include <stdio.h>
#include <math.h>

// Function to calculate logarithm (base 10)
double logBase10(double x) {
    return log10(x);
}

// Function to calculate natural logarithm (base e)
double logBaseE(double x) {
    return log(x);
}

// Function to calculate custom base logarithm
double logCustomBase(double x, double base) {
    return log(x) / log(base);
}

int main() {
    double number, base;

    printf("Enter a number: ");
    scanf("%lf", &number);

    // Logarithm (base 10)
    printf("Logarithm (base 10) of %.2lf = %.4lf\n", number, logBase10(number));

    // Natural logarithm (base e)
    printf("Natural Logarithm (base e) of %.2lf = %.4lf\n", number, logBaseE(number));

    // Custom base logarithm
    printf("Enter the custom base for logarithm: ");
    scanf("%lf", &base);
    printf("Logarithm (base %.2lf) of %.2lf = %.4lf\n", base, number, logCustomBase(number, base));

    return 0;
}
