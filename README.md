# Assignment 2 -C-programming 2
1. What do you mean by Structures?

Definition:
A structure in C is a user-defined data type that allows you to combine data items of different kinds (like int, float, char, etc.) under one name.

Example Code:

#include <stdio.h>

// Define structure
struct Student {
    int id;
    char name[50];
    float marks;
};

int main() {
    struct Student s1 = {1, "Rajat", 89.5};

    printf("Student ID: %d\n", s1.id);
    printf("Name: %s\n", s1.name);
    printf("Marks: %.2f\n", s1.marks);

    return 0;
}

Output:

Student ID: 1
Name: Rajat
Marks: 89.50


---

2. What do you mean by Array & Pointers Array?

Definition:

Array: A collection of similar data types stored in contiguous memory locations.

Pointer Array: An array that stores the address of variables (i.e., array of pointers).


Example Code:

#include <stdio.h>

int main() {
    int arr[3] = {10, 20, 30};      // Normal array
    int *ptr[3];                    // Array of pointers

    for(int i = 0; i < 3; i++) {
        ptr[i] = &arr[i];           // Storing address of each element
    }

    printf("Normal Array Elements:\n");
    for(int i = 0; i < 3; i++) {
        printf("%d ", arr[i]);
    }

    printf("\nUsing Pointer Array:\n");
    for(int i = 0; i < 3; i++) {
        printf("%d ", *ptr[i]);     // Accessing values using pointers
    }

    return 0;
}

Output:

Normal Array Elements:
10 20 30
Using Pointer Array:
10 20 30


---

3. Compare Two Structure Variables (Equal & Not Equal)

> ⚠ In C, structures cannot be compared directly using == or !=.
We must compare each member individually.



Example Code:

#include <stdio.h>
#include <string.h>

struct Student {
    int id;
    char name[50];
};

int main() {
    struct Student s1 = {1, "Rajat"};
    struct Student s2 = {2, "Aman"};

    if (s1.id == s2.id && strcmp(s1.name, s2.name) == 0)
        printf("Structures are Equal\n");
    else
        printf("Structures are Not Equal\n");

    return 0;
}

Output:

Structures are Not Equal


---

4. Perform Arithmetic Operations on Structures

We can perform arithmetic operations on structure members, not on the structure directly.

Example Code:

#include <stdio.h>

struct Numbers {
    int a;
    int b;
};

int main() {
    struct Numbers n = {10, 5};
    int sum, diff, prod, div;

    sum = n.a + n.b;
    diff = n.a - n.b;
    prod = n.a * n.b;
    div = n.a / n.b;

    printf("Sum = %d\n", sum);
    printf("Difference = %d\n", diff);
    printf("Product = %d\n", prod);
    printf("Division = %d\n", div);

    return 0;
}

Output:

Sum = 15
Difference = 5
Product = 50
Division = 2


---
