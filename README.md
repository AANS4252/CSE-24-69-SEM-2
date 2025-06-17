#include<stdio.h>
int main()
{
  int a=50 , b=20,c;
int*ptr=&a;

  // Arithmetic Operators

    printf ("Arithmetic Operators:\n");
    printf ("a + b = %d\n", a + b);
    printf ("a - b = %d\n", a - b);
    printf ("a * b = %d\n", a * b);
    printf ("a / b = %d\n", a / b);
    printf ("a %% b = %d\n\n", a % b);

    // Relational Operators

    printf ("Relational Operators:\n");
    printf ("a == b: %d\n", a == b);
    printf ("a != b: %d\n", a != b);
    printf ("a > b: %d\n", a > b);
    printf ("a < b: %d\n", a < b);
    printf ("a >= b: %d\n", a >= b);
    printf ("a <= b: %d\n\n", a <= b);


    // Logical Operators

    printf ("Logical Operators:\n");
    printf ("(a > 0 && b > 0): %d\n", (a > 0 && b > 0));
    printf ("(a > 0 || b < 0): %d\n", (a > 0 || b < 0));
    printf ("!(a == b): %d\n\n", !(a == b));


    // Bitwise Operators

    printf ("Bitwise Operators:\n");
    printf ("a & b = %d\n", a & b);
    printf ("a | b = %d\n", a | b);
    printf ("a ^ b = %d\n", a ^ b);
    printf ("~a = %d\n", ~a);
    printf ("a << 1 = %d\n", a << 1);
    printf ("a >> 1 = %d\n\n", a >> 1);


    // Assignment Operators

    printf ("Assignment Operators:\n");
    c = a;
    c += b;
    printf ("c += b: %d\n", c);
    c -= b;
    printf ("c -= b: %d\n", c);
    c *= b;
    printf ("c *= b: %d\n", c);
    c /= b;
    printf ("c /= b: %d\n", c);
    c %= b;
    printf ("c %%= b: %d\n\n", c);


    // Increment/Decrement Operators

    printf ("Increment/Decrement Operators:\n");
    printf ("a++ = %d\n", a++);
    printf ("Now a = %d\n", a);
    printf ("++a = %d\n", ++a);
    printf ("a-- = %d\n", a--);
    printf ("Now a = %d\n", a);
    printf ("--a = %d\n\n", --a);


    // Conditional (Ternary) Operator

    printf ("Conditional Operator:\n");
    int max = (a > b) ? a : b;
    printf ("Max of a and b: %d\n\n", max);


    // sizeof Operator

    printf ("sizeof Operator:\n");
    printf ("Size of int: %d bytes\n", sizeof(int));
    printf ("Size of float: %f bytes\n", sizeof(float));
    printf ("Size of char: %c bytes\n\n", sizeof(char));


    // Address Operators

    printf ("Pointer Operators:\n");
    printf ("Address of a: %d\n", &a);
   
    return 0;
}


//Implicit type conversion
#include <stdio.h>

int main() {
    int var1 = 19;
    char var2 = 'A';
    var1= var1 + var2; 
    float var3 = var1 +1.0; 
    printf("var1 = %d, var3 = %f", var1, var3);
  
    return 0;
}


// Explicit type conversion
#include <stdio.h>

int main() {
   double var1 = 1.7;

    int add= (int)var1 + 3; 
   
    printf("Addition = %d", add);
    return 0;
}

//Use if-else to check whether a number is even or odd
 #include <stdio.h>
int main() {
    int num;
    printf("Enter an integer: ");
    scanf("%d", &num);

    if (num % 2 == 0) {
        printf("%d is even.\n", num);
    } else {
        printf("%d is odd.\n", num);
    }
    return 0;
}



//Use nesting of if-else to compare three numbers
#include <stdio.h>
int main() {
    int a, b, c;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    if (a > b) {
        if (a > c) {
            printf("%d is the largest number.\n", a);
        } else {
            printf("%d is the largest number.\n", c);
        }
    } else {
        if (b > c) {
            printf("%d is the largest number.\n", b);
        } else {
            printf("%d is the largest number.\n", c);
        }
    }
    return 0;
}


//Find roots of a quadratic equation
#include <stdio.h>
#include <math.h>
int main() {
    float a, b, c, discriminant, root1, root2, realPart, imagPart;
    printf("Enter coefficients a, b and c: ");
    scanf("%f %f %f", &a, &b, &c);
    discriminant = b * b - 4 * a * c;
    if (discriminant > 0) {
        root1 = (-b + sqrt(discriminant)) / (2 * a);
        root2 = (-b - sqrt(discriminant)) / (2 * a);
        printf("Roots are real and different.\n");
        printf("Root 1 = %.2f\n", root1);
        printf("Root 2 = %.2f\n", root2);
    }
    else if (discriminant == 0) {
        root1 = root2 = -b / (2 * a);
        printf("Roots are real and equal.\n");
        printf("Root 1 = Root 2 = %.2f\n", root1);
    }
    else {
        realPart = -b / (2 * a);
        imagPart = sqrt(-discriminant) / (2 * a);
        printf("Roots are complex and imaginary.\n");
        printf("Root 1 = %.2f + %.2fi\n", realPart, imagPart);
        printf("Root 2 = %.2f - %.2fi\n", realPart, imagPart);
    }
    return 0;
}



//Use if-else with relational and logical operators (grading according to percentage of a student).
#include <stdio.h>
int main() {
    float percentage;
    printf("Enter your percentage: ");
    scanf("%f", &percentage);
    if (percentage >= 90 && percentage <= 100) {
        printf("Grade: A\n");
    } 
    else if (percentage >= 80 && percentage < 90) {
        printf("Grade: B\n");
    } 
    else if (percentage >= 70 && percentage < 80) {
        printf("Grade: C\n");
    } 
    else if (percentage >= 60 && percentage < 70) {
        printf("Grade: D\n");
    } 
    else if (percentage >= 50 && percentage < 60) {
        printf("Grade: E\n");
    } 
    else if (percentage >= 0 && percentage < 50) {
        printf("Grade: F (Fail)\n");
    } 
    else {
        printf("Invalid percentage entered.\n");
    }
    return 0;
}


//Use switch-case to display Salaam when user enters 1, Aadaab when user enters 2, Hello when user enters 3 and Incorrect Option when user enters any other number
#include <stdio.h>
int main() {
    int choice;

    printf("Enter a number (1, 2, or 3): ");
    scanf("%d", &choice);
    switch (choice) {
        case 1:
            printf("Salaam\n");
            break;
        case 2:
            printf("Aadaab\n");
            break;
        case 3:
            printf("Hello\n");
            break;
        default:
            printf("Incorrect Option\n");
            break;
    }

    return 0;
}























