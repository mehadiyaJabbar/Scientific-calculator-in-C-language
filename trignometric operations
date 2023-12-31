#include <stdio.h>
#include <math.h>

int main() {
    int choice;
    double angle, result;

    while (1) {
        // Display menu
        printf("\nScientific Calculator Menu:\n");
        printf("1. Sine\n");
        printf("2. Cosine\n");
        printf("3. Tangent\n");
        printf("4. Arcsine\n");
        printf("5. Arccosine\n");
        printf("6. Arctangent\n");
        printf("7. Exit\n");

        // User input for choice
        printf("Enter your choice (1-7): ");
        scanf("%d", &choice);

        // Exit condition
        if (choice == 7) {
            printf("Exiting the calculator. Goodbye!\n");
            break;
        }

        // Input angle in degrees
        printf("Enter the angle in degrees: ");
        scanf("%lf", &angle);

        // Convert angle to radians
        double radianAngle = angle * M_PI / 180.0;

        // Perform the selected operation
        switch (choice) {
            case 1:
                result = sin(radianAngle);
                printf("Sine of %.2lf degrees is %.4lf\n", angle, result);
                break;
            case 2:
                result = cos(radianAngle);
                printf("Cosine of %.2lf degrees is %.4lf\n", angle, result);
                break;
            case 3:
                result = tan(radianAngle);
                printf("Tangent of %.2lf degrees is %.4lf\n", angle, result);
                break;
            case 4:
                result = asin(sin(radianAngle));
                printf("Arcsine of %.2lf degrees is %.4lf\n", angle, result * 180.0 / M_PI);
                break;
            case 5:
                result = acos(cos(radianAngle));
                printf("Arccosine of %.2lf degrees is %.4lf\n", angle, result * 180.0 / M_PI);
                break;
            case 6:
                result = atan(tan(radianAngle));
                printf("Arctangent of %.2lf degrees is %.4lf\n", angle, result * 180.0 / M_PI);
                break;
            default:
                printf("Invalid choice. Please enter a number between 1 and 7.\n");
        }
    }

    return 0;
}
