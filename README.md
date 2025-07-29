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

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
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
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

// Explicit type conversion
#include <stdio.h>

int main() {
   double var1 = 1.7;

    int add= (int)var1 + 3; 
   
    printf("Addition = %d", add);
    return 0;
}
----------------------------------------------------------------
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

----------------------------------------------------------------

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

----------------------------------------------------------------


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

----------------------------------------------------------------


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

----------------------------------------------------------------

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

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
//Array

//Display contents of an integer array. 

#include <stdio.h>
int main() {
    int arr[] = {10, 20, 30, 40, 50};  
    int n = sizeof(arr) / sizeof(arr[0]);  
    printf("Array elements are:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]); 
    }
    return 0;
    }


----------------------------------------------------------------
    


//Input an integer array from the user and display the same. 

#include <stdio.h>
int main() {
    int arr[100], n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);  // User inputs how many integers they want to store
    printf("Enter %d integers:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);  // Read each integer into the array
    }
        printf("Array elements are:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);  // Display each element
    }
    return 0;
}


----------------------------------------------------------------
//Display contents of an integer array in reverse order.

#include <stdio.h>
int main() {
    int arr[100], n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
  
  printf("Enter %d integers:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    printf("Array in reverse order:\n");
    for (int i = n - 1; i >= 0; i--) {
        printf("%d ", arr[i]);
    }
    return 0;
}

----------------------------------------------------------------
//Display contents of a character array. 

#include <stdio.h>

int main() {
    char arr[] = {'H', 'e', 'l', 'l', 'o', '\0'};  // Character array with null terminator
    printf("Character array content: %s\n", arr);

    return 0;
}

----------------------------------------------------------------

//Input a string from the user and display the same. 

#include <stdio.h>

int main() {
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);  // Read string input (no spaces)

    printf("You entered: %s\n", str);

    return 0;
}  

-----------------{OR}--------------------

#include <stdio.h>

int main() {
    char str[100];

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Reads entire line including spaces

    printf("You entered: %s", str);

    return 0;
  }


----------------------------------------------------------------

//Input a string from the user and find its length (without using the string library).

#include <stdio.h>

int main() {
    char str[100];
    int length = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Read string with spaces

    // Manually calculate length (excluding '\0')
    while (str[length] != '\0') {
        if (str[length] == '\n') {
            break;  // Stop at newline (from Enter key)
        }
        length++;
    }

    printf("Length of the string: %d\n", length);

    return 0;
}

----------------------------------------------------------------


//Input a string from the user and display it in reverse order.

#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int length = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Remove newline character if present
    str[strcspn(str, "\n")] = '\0';

    // Calculate length manually
    while (str[length] != '\0') {
        length++;
    }

    printf("Reversed string: ");
    for (int i = length - 1; i >= 0; i--) {
        printf("%c", str[i]);
    }
    printf("\n");

    return 0;
}


----------------------------------------------------------------


//Demonstrate the use of string library functions: strlen(), strcpy(), strrev(), strcat(), strcmp() etc. using examples.

#include <stdio.h>
#include <string.h>

int main() {
    char str1[100] = "Hello";
    char str2[100] = "World";
    char str3[100];

    // strlen(): Length of string
    printf("Length of '%s' is %lu\n", str1, strlen(str1));

    // strcpy(): Copy string
    strcpy(str3, str1);
    printf("After strcpy, str3 = %s\n", str3);

    
    // strcat(): Concatenate strings
    strcat(str3, str2);
    printf("After strcat, str3 = %s\n", str3);

    // strcmp(): Compare strings
    int cmp = strcmp(str1, str2);
    if (cmp == 0) {
        printf("'%s' and '%s' are equal.\n", str1, str2);
    } else if (cmp < 0) {
        printf("'%s' is less than '%s'.\n", str1, str2);
    } else {
        printf("'%s' is greater than '%s'.\n", str1, str2);
    }

    return 0;
}





------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

    //Loops
    
//Display the series: 1 2 3 4 5 .... n (using loops)


#include <stdio.h>
int main() {
    int n, i;
    printf("Enter n: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        printf("%d ", i);
    }
    return 0;
}
----------------------------------------------------------------
//Display the series: n n-1 n-2 …. 3 2 1  (using loops)

#include <stdio.h>
int main() {
    int n, i;
    printf("Enter n: ");
    scanf("%d", &n);

    for (i = n; i >= 1; i--) {
        printf("%d ", i);
    }
    return 0;
}

----------------------------------------------------------------

//Display all even numbers from 1 to 100.  (using loop and if)
#include <stdio.h>

int main() {
    int i;
    for (i = 1; i <= 100; i++) {
        if (i % 2 == 0) {
            printf("%d ", i);
        }
    }
    return 0;
    }
    
    
    ----------------------------------------------------------------
//Find sum of series: 1 2 3 4 5 .... n 


#include <stdio.h>

int main() {
    int n, i, sum = 0;
    printf("Enter n: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        sum += i;
    }

    printf("Sum = %d\n", sum);
    return 0;
}

----------------------------------------------------------------

//Find product of series: 1 2 3 4 5 .... n .

#include <stdio.h>

int main() {
    int n, i;
    unsigned long long product = 1;
    printf("Enter n: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        product *= i;
    }

    printf("Product = %llu\n", product);
    return 0;
}

----------------------------------------------------------------

//Finding the factorial of a number entered by the user.
#include <stdio.h>

int main() {
    int n, i;
    unsigned long long fact = 1;
    printf("Enter a number: ");
    scanf("%d", &n);

    if (n < 0)
        printf("Factorial not defined for negative numbers.\n");
    else {
        for (i = 1; i <= n; i++) {
            fact *= i;
        }
        printf("Factorial = %llu\n", fact);
    }
    return 0;
}

----------------------------------------------------------------

//Finding all the factors of a natural number.
#include <stdio.h>
int main() {
    int n, i;
    printf("Enter a natural number: ");
    scanf("%d", &n);

    printf("Factors of %d are: ", n);
    for (i = 1; i <= n; i++) {
        if (n % i == 0) {
            printf("%d ", i);
        }
    }
    return 0;
}


----------------------------------------------------------------

//Checking whether a given number is prime.

#include <stdio.h>

int main() {
    int n, i, isPrime = 1;
    printf("Enter a number: ");
    scanf("%d", &n);

    if (n <= 1) {
        isPrime = 0;
    } else {
        for (i = 2; i <= n / 2; i++) {
            if (n % i == 0) {
                isPrime = 0;
                break;
            }
        }
    }

    if (isPrime)
        printf("%d is a prime number.\n", n);
    else
        printf("%d is not a prime number.\n", n);

    return 0;
}

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  

//POINTERS

//Swap Two Numbers Using Call-by-Reference

#include <stdio.h>

void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 5, y = 10;
    printf("Before Swap: x = %d, y = %d\n", x, y);
    swap(&x, &y);  // Passing addresses
    printf("After Swap: x = %d, y = %d\n", x, y);
    return 0;
}


----------------------------------------------------------------

//Display Contents of an Array Using Pointers

#include <stdio.h>

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int *ptr = arr;

    printf("Array elements using pointers:\n");
    for (int i = 0; i < 5; i++) {
        printf("%d ", *(ptr + i));
    }

    return 0;
}



----------------------------------------------------------------

//Display a String in Reverse Using Pointers

#include <stdio.h>
#include <string.h>

int main() {
    char str[] = "pointer";
    char *ptr = str;
    int len = strlen(str);

    printf("String in reverse: ");
    for (int i = len - 1; i >= 0; i--) {
        printf("%c", *(ptr + i));
    }

    return 0;
}

----------------------------------------------------------------
//Check if a String is Palindrome Using Pointers

#include <stdio.h>
#include <string.h>

int isPalindrome(char *str) {
    char *start = str;
    char *end = str + strlen(str) - 1;

    while (start < end) {
        if (*start != *end)
            return 0;
        start++;
        end--;
    }
    return 1;
}

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);

    if (isPalindrome(str))
        printf("The string is a palindrome.\n");
    else
        printf("The string is not a palindrome.\n");

    return 0;
}


----------------------------------------------------------------

//Sort an Integer Array Using Functions and Pointers

#include <stdio.h>

void sort(int *arr, int size) {
    for (int i = 0; i < size - 1; i++) {
        for (int j = 0; j < size - i - 1; j++) {
            if (*(arr + j) > *(arr + j + 1)) {
                int temp = *(arr + j);
                *(arr + j) = *(arr + j + 1);
                *(arr + j + 1) = temp;
            }
        }
    }
}

int main() {
    int arr[] = {45, 23, 89, 12, 78};
    int size = sizeof(arr) / sizeof(arr[0]);

    sort(arr, size);

    printf("Sorted array: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", *(arr + i));
    }

    return 0;
}


 











