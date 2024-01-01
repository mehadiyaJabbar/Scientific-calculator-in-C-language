#include <stdio.h>
#include <math.h>

// Function prototypes
double add(double a, double b);
double subtract(double a, double b);
double multiply(double a, double b);
double divide(double a, double b);
double exponentiation(double base, double exponent);
double squareRoot(double x);
double cubeRoot(double x);
double nthRoot(double x, double n);
double factorial(double x);
double absoluteValue(double x);

int main() {
    int choice;
    double num1, num2, result;

    do {
        // Display menu
        printf("\nScientific Calculator Menu:\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exponentiation\n");
        printf("6. Square Root\n");
        printf("7. Cube Root\n");
        printf("8. nth Root\n");
        printf("9. Factorial\n");
        printf("10. Absolute Value\n");
        printf("0. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        // Perform the selected operation
        switch (choice) {
            case 1:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                result = add(num1, num2);
                break;
            case 2:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                result = subtract(num1, num2);
                break;
            case 3:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                result = multiply(num1, num2);
                break;
            case 4:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                result = divide(num1, num2);
                break;
            case 5:
                printf("Enter base and exponent: ");
                scanf("%lf %lf", &num1, &num2);
                result = exponentiation(num1, num2);
                break;
            case 6:
                printf("Enter a number: ");
                scanf("%lf", &num1);
                result = squareRoot(num1);
                break;
            case 7:
                printf("Enter a number: ");
                scanf("%lf", &num1);
                result = cubeRoot(num1);
                break;
            case 8:
                printf("Enter a number and root (n): ");
                scanf("%lf %lf", &num1, &num2);
                result = nthRoot(num1, num2);
                break;
            case 9:
                printf("Enter a number: ");
                scanf("%lf", &num1);
                result = factorial(num1);
                break;
            case 10:
                printf("Enter a number: ");
                scanf("%lf", &num1);
                result = absoluteValue(num1);
                break;
            case 0:
                printf("Exiting the calculator. Goodbye!\n");
                return 0;
            default:
                printf("Invalid choice. Please enter a valid option.\n");
                continue;
        }

        // Display the result
        printf("Result: %lf\n", result);

    } while (1); // Infinite loop for calculator operations

    return 0;
}

// Function definitions

double add(double a, double b) {
    return a + b;
}

double subtract(double a, double b) {
    return a - b;
}

double multiply(double a, double b) {
    return a * b;
}

double divide(double a, double b) {
    if (b != 0) {
        return a / b;
    } else {
        printf("Error: Division by zero!\n");
        return NAN; // Not a Number
    }
}

double exponentiation(double base, double exponent) {
    return pow(base, exponent);
}

double squareRoot(double x) {
    if (x >= 0) {
        return sqrt(x);
    } else {
        printf("Error: Cannot calculate square root of a negative number!\n");
        return NAN;
    }
}

double cubeRoot(double x) {
    return cbrt(x);
}

double nthRoot(double x, double n) {
    if (x >= 0 || (n == 2 && x < 0)) {
        return pow(x, 1 / n);
    } else {
        printf("Error: Cannot calculate nth root of a negative number!\n");
        return NAN;
    }
}

double factorial(double x) {
    if (x < 0) {
        printf("Error: Cannot calculate factorial of a negative number!\n");
        return NAN;
    }

    double result = 1;
    for (int i = 2; i <= x; ++i) {
        result *= i;
    }

    return result;
}

double absoluteValue(double x) {
    return fabs(x);
}
