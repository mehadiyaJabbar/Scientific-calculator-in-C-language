#include <stdio.h>

typedef struct {
    double real;
    double imag;
} Complex;

// Function prototypes
Complex add(Complex num1, Complex num2);
Complex subtract(Complex num1, Complex num2);
Complex multiply(Complex num1, Complex num2);
Complex divide(Complex num1, Complex num2);
Complex conjugate(Complex num);

int main() {
    Complex num1, num2, result;

    // Input for the first complex number
    printf("Enter real and imaginary parts of the first complex number:\n");
    scanf("%lf %lf", &num1.real, &num1.imag);

    // Input for the second complex number
    printf("Enter real and imaginary parts of the second complex number:\n");
    scanf("%lf %lf", &num2.real, &num2.imag);

    // Addition
    result = add(num1, num2);
    printf("Sum: %.2lf + %.2lfi\n", result.real, result.imag);

    // Subtraction
    result = subtract(num1, num2);
    printf("Difference: %.2lf + %.2lfi\n", result.real, result.imag);

    // Multiplication
    result = multiply(num1, num2);
    printf("Product: %.2lf + %.2lfi\n", result.real, result.imag);

    // Division
    result = divide(num1, num2);
    printf("Quotient: %.2lf + %.2lfi\n", result.real, result.imag);

    // Conjugate
    result = conjugate(num1);
    printf("Conjugate of the first complex number: %.2lf + %.2lfi\n", result.real, result.imag);

    return 0;
}

// Function to add two complex numbers
Complex add(Complex num1, Complex num2) {
    Complex result;
    result.real = num1.real + num2.real;
    result.imag = num1.imag + num2.imag;
    return result;
}

// Function to subtract two complex numbers
Complex subtract(Complex num1, Complex num2) {
    Complex result;
    result.real = num1.real - num2.real;
    result.imag = num1.imag - num2.imag;
    return result;
}

// Function to multiply two complex numbers
Complex multiply(Complex num1, Complex num2) {
    Complex result;
    result.real = num1.real * num2.real - num1.imag * num2.imag;
    result.imag = num1.real * num2.imag + num1.imag * num2.real;
    return result;
}

// Function to divide two complex numbers
Complex divide(Complex num1, Complex num2) {
    Complex result;
    double denominator = num2.real * num2.real + num2.imag * num2.imag;
    result.real = (num1.real * num2.real + num1.imag * num2.imag) / denominator;
    result.imag = (num1.imag * num2.real - num1.real * num2.imag) / denominator;
    return result;
}

// Function to find the conjugate of a complex number
Complex conjugate(Complex num) {
    Complex result;
    result.real = num.real;
    result.imag = -num.imag;
    return result;
}
