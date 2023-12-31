#include <stdio.h>

// Function prototypes
void addMatrices(int rows, int cols, int matrix1[10][10], int matrix2[10][10], int result[10][10]);
void subtractMatrices(int rows, int cols, int matrix1[10][10], int matrix2[10][10], int result[10][10]);
void multiplyMatrices(int rows1, int cols1, int rows2, int cols2, int matrix1[10][10], int matrix2[10][10], int result[10][10]);
void transposeMatrix(int rows, int cols, int matrix[10][10], int result[10][10]);
int determinant(int n, int matrix[10][10]);
void inverse(int n, int matrix[10][10], float result[10][10]);

int main() {
    int choice;
    
    do {
        printf("Matrix Calculator\n");
        printf("1. Addition of matrices\n");
        printf("2. Subtraction of matrices\n");
        printf("3. Multiplication of matrices\n");
        printf("4. Transposition of a matrix\n");
        printf("5. Determinant of a matrix\n");
        printf("6. Inverse of a matrix\n");
        printf("0. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice >= 1 && choice <= 6) {
            int matrix1[10][10], matrix2[10][10], result[10][10], rows1, cols1, rows2, cols2;

            printf("Enter the number of rows and columns of matrix 1: ");
            scanf("%d %d", &rows1, &cols1);

            printf("Enter the elements of matrix 1:\n");
            for (int i = 0; i < rows1; ++i) {
                for (int j = 0; j < cols1; ++j) {
                    scanf("%d", &matrix1[i][j]);
                }
            }

            if (choice != 4 && choice != 5 && choice != 6) {
                printf("Enter the number of rows and columns of matrix 2: ");
                scanf("%d %d", &rows2, &cols2);

                printf("Enter the elements of matrix 2:\n");
                for (int i = 0; i < rows2; ++i) {
                    for (int j = 0; j < cols2; ++j) {
                        scanf("%d", &matrix2[i][j]);
                    }
                }
            }

            switch (choice) {
                case 1:
                    addMatrices(rows1, cols1, matrix1, matrix2, result);
                    break;
                case 2:
                    subtractMatrices(rows1, cols1, matrix1, matrix2, result);
                    break;
                case 3:
                    multiplyMatrices(rows1, cols1, rows2, cols2, matrix1, matrix2, result);
                    break;
                case 4:
                    transposeMatrix(rows1, cols1, matrix1, result);
                    break;
                case 5:
                    printf("Determinant of matrix 1: %d\n", determinant(rows1, matrix1));
                    break;
                case 6:
                    {
                        float inverseResult[10][10];
                        inverse(rows1, matrix1, inverseResult);
                        printf("Inverse of matrix 1:\n");
                        for (int i = 0; i < rows1; ++i) {
                            for (int j = 0; j < cols1; ++j) {
                                printf("%.2f\t", inverseResult[i][j]);
                            }
                            printf("\n");
                        }
                    }
                    break;
                default:
                    printf("Invalid choice\n");
                    break;
            }
        }
        else if (choice != 0) {
            printf("Invalid choice\n");
        }
    } while (choice != 0);

    printf("Exiting the program\n");

    return 0;
}

void addMatrices(int rows, int cols, int matrix1[10][10], int matrix2[10][10], int result[10][10]) {
    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            result[i][j] = matrix1[i][j] + matrix2[i][j];
        }
    }

    printf("Resultant matrix:\n");
    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            printf("%d\t", result[i][j]);
        }
        printf("\n");
    }
}

void subtractMatrices(int rows, int cols, int matrix1[10][10], int matrix2[10][10], int result[10][10]) {
    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            result[i][j] = matrix1[i][j] - matrix2[i][j];
        }
    }

    printf("Resultant matrix:\n");
    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            printf("%d\t", result[i][j]);
        }
        printf("\n");
    }
}

void multiplyMatrices(int rows1, int cols1, int rows2, int cols2, int matrix1[10][10], int matrix2[10][10], int result[10][10]) {
    if (cols1 != rows2) {
        printf("Error: Number of columns in matrix 1 must be equal to the number of rows in matrix 2 for multiplication\n");
        return;
    }

    for (int i = 0; i < rows1; ++i) {
        for (int j = 0; j < cols2; ++j) {
            result[i][j] = 0;
            for (int k = 0; k < cols1; ++k) {
                result[i][j] += matrix1[i][k] * matrix2[k][j];
            }
        }
    }

    printf("Resultant matrix:\n");
    for (int i = 0; i < rows1; ++i) {
        for (int j = 0; j < cols2; ++j) {
            printf("%d\t", result[i][j]);
        }
        printf("\n");
    }
}

void transposeMatrix(int rows, int cols, int matrix[10][10], int result[10][10]) {
    for (int i = 0; i < cols; ++i) {
        for (int j = 0; j < rows; ++j) {
            result[i][j] = matrix[j][i];
        }
    }

    printf("Resultant matrix (transpose):\n");
    for (int i = 0; i < cols; ++i) {
        for (int j = 0; j < rows; ++j) {
            printf("%d\t", result[i][j]);
        }
        printf("\n");
    }
}

int determinant(int n, int matrix[10][10]) {
    if (n == 1) {
        return matrix[0][0];
    }
    else if (n == 2) {
        return (matrix[0][0] * matrix[1][1]) - (matrix[0][1] * matrix[1][0]);
    }
    else {
        int det = 0;
        for (int i = 0; i < n; ++i) {
            int submatrix[10][10], sign = (i % 2 == 0) ? 1 : -1;

            // Create submatrix
            for (int j = 0; j < n - 1; ++j) {
                for (int k = 0, l = 0; k < n; ++k) {
                    if (k == i) {
                        continue;
                    }
                    submatrix[j][l] = matrix[j + 1][k];
                    ++l;
                }
            }

            // Recursive call for determinant of submatrix
            det += sign * matrix[0][i] * determinant(n - 1, submatrix);
        }
        return det;
    }
}

void inverse(int n, int matrix[10][10], float result[10][10]) {
    int det = determinant(n, matrix);
    if (det == 0) {
        printf("Inverse does not exist because the determinant is zero\n");
        return;
    }

    for (int i = 0; i < n; ++i) {
        for (int j = 0; j < n; ++j) {
            int sign = ((i + j) % 2 == 0) ? 1 : -1;
            int submatrix[10][10], submatrixResult[10][10];

            // Create submatrix
            for (int k = 0; k < n; ++k) {
                for (int l = 0; l < n; ++l) {
                    if (k != i && l != j) {
                        submatrixResult[(k < i) ? k : k - 1][(l < j) ? l : l - 1] = matrix[k][l];
                    }
                }
            }

            // Calculate determinant of submatrix
            result[j][i] = sign * determinant(n - 1, submatrixResult) / (float)det;
        }
    }
}
