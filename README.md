

# Pointer Examples in C

A simple C program demonstrating essential pointer concepts including:

* Array traversal using pointers
* Swapping two integers via pointers
* Dynamic string manipulation and concatenation using `malloc`, `strcpy`, and `strcat`

## Features

* Traverse and print elements of an integer array using pointer arithmetic.
* Swap two integers by passing their addresses to a function.
* Dynamically allocate memory for strings, copy content, and concatenate them safely.
* Proper memory management with `malloc` and `free`.

## How to Compile and Run

1. Save the code into a file, e.g., `pointer_examples.c`.
2. Compile using GCC:

```bash
gcc pointer_examples.c -o pointer_examples
```

3. Run the executable:

```bash
./pointer_examples
```

## Sample Output

```
--- Array Traversal ---
Array elements: 10 20 30 40 50 

--- Swapping Numbers ---
Before swap: num1 = 100, num2 = 200
After swap: num1 = 200, num2 = 100

--- Dynamic String Manipulation ---
Initial strings: dyn_str1 = "Hello", dyn_str2 = "World"
Concatenated string: "Hello World"
```

## Code Explanation

* **Array traversal:** Uses pointer arithmetic (`*(ptr + i)`) to access array elements.
* **Swapping integers:** Function `swap_integers` takes pointers to integers and swaps their values using a temporary variable.
* **Dynamic strings:** Allocates memory on the heap with `malloc`, copies strings using `strcpy`, concatenates with `strcat`, and frees memory after use.
* Handles errors by checking if `malloc` returns `NULL`.

## Notes

* Ensure your system has a C compiler like GCC.
* Run the program in an environment that supports standard input/output.
* The program demonstrates basic memory management and pointer usage for beginners.

---


