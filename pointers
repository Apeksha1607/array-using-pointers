#include <stdio.h>
#include <stdlib.h> // For malloc, free
#include <string.h> // For strlen, strcpy, strcat

// Function to swap two integers using pointers
void swap_integers(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    // 1. Array Traversal using Pointers
    printf("--- Array Traversal ---\n");
    int arr[] = {10, 20, 30, 40, 50};
    int size = sizeof(arr) / sizeof(arr[0]);
    int *ptr = arr; // Pointer to the first element of the array

    printf("Array elements: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", *(ptr + i)); // Accessing elements using pointer arithmetic
    }
    printf("\n\n");

    // 2. Swapping Numbers using Pointers
    printf("--- Swapping Numbers ---\n");
    int num1 = 100, num2 = 200;
    printf("Before swap: num1 = %d, num2 = %d\n", num1, num2);
    swap_integers(&num1, &num2); // Pass addresses to the swap function
    printf("After swap: num1 = %d, num2 = %d\n\n", num1, num2);

    // 3. Dynamic String Manipulation using Pointers
    printf("--- Dynamic String Manipulation ---\n");
    char *dyn_str1 = (char *)malloc(sizeof(char) * 20); // Allocate memory for 20 characters
    if (dyn_str1 == NULL) {
        perror("Memory allocation failed");
        return 1;
    }
    strcpy(dyn_str1, "Hello");

    char *dyn_str2 = (char *)malloc(sizeof(char) * 20);
    if (dyn_str2 == NULL) {
        perror("Memory allocation failed");
        free(dyn_str1); // Free previously allocated memory
        return 1;
    }
    strcpy(dyn_str2, "World");

    printf("Initial strings: dyn_str1 = \"%s\", dyn_str2 = \"%s\"\n", dyn_str1, dyn_str2);

    // Concatenate strings
    char *concatenated_str = (char *)malloc(sizeof(char) * (strlen(dyn_str1) + strlen(dyn_str2) + 2)); // +2 for space and null terminator
    if (concatenated_str == NULL) {
        perror("Memory allocation failed");
        free(dyn_str1);
        free(dyn_str2);
        return 1;
    }
    strcpy(concatenated_str, dyn_str1);
    strcat(concatenated_str, " ");
    strcat(concatenated_str, dyn_str2);
    printf("Concatenated string: \"%s\"\n", concatenated_str);

    // Free allocated memory
    free(dyn_str1);
    free(dyn_str2);
    free(concatenated_str);

    return 0;
}
