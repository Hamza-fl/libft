# libft

## Project Description

This repository contains `libft`, my own implementation of a standard C library.  The goal is to recreate commonly used functions, enhancing my understanding of low-level programming and memory management in C.

## Features and Functionality

This library includes a variety of functions commonly found in the standard C library.  While a complete list is best found by reviewing the header file (`libft.h`), here are some key categories and examples:

*   **Memory Management:** Functions for allocating, freeing, and manipulating memory.
    *   `ft_memset`: Fills a block of memory with a specific value.
    *   `ft_bzero`: Sets a block of memory to zero.
    *   `ft_memcpy`: Copies a block of memory from one location to another.
    *   `ft_memmove`: Copies a block of memory, handling overlapping source and destination regions.
    *   `ft_memchr`: Locates a character within a block of memory.
    *   `ft_memcmp`: Compares two blocks of memory.
    *   `ft_calloc`: Allocates memory and initializes it to zero.

*   **String Manipulation:** Functions for working with strings.
    *   `ft_strlen`: Calculates the length of a string.
    *   `ft_strlcpy`: Copies a string with size limitation and NULL termination guarantee.
    *   `ft_strlcat`: Appends a string to another string with size limitation and NULL termination guarantee.
    *   `ft_strchr`: Locates the first occurrence of a character in a string.
    *   `ft_strrchr`: Locates the last occurrence of a character in a string.
    *   `ft_strnstr`: Locates a substring within a string.
    *   `ft_strncmp`: Compares two strings up to a specified number of characters.
    *   `ft_strdup`: Duplicates a string.

*   **Character Handling:** Functions for classifying and converting characters.
    *   `ft_isalpha`: Checks if a character is an alphabetic character.
    *   `ft_isdigit`: Checks if a character is a digit.
    *   `ft_isalnum`: Checks if a character is an alphanumeric character.
    *   `ft_isascii`: Checks if a character is an ASCII character.
    *   `ft_isprint`: Checks if a character is a printable character.
    *   `ft_toupper`: Converts a character to uppercase.
    *   `ft_tolower`: Converts a character to lowercase.

*   **Integer Conversion:**
    *   `ft_atoi`: Converts a string to an integer.

*   **Output:**
    *   `ft_putchar_fd`: Writes a character to a file descriptor.
    *   `ft_putstr_fd`: Writes a string to a file descriptor.
    *   `ft_putendl_fd`: Writes a string to a file descriptor, followed by a newline.
    *   `ft_putnbr_fd`: Writes an integer to a file descriptor.

*   **Additional Functions:**
    *   `ft_substr`: Creates a substring from a string.
    *   `ft_strjoin`: Concatenates two strings.
    *   `ft_strtrim`: Trims leading and trailing characters from a string.
    *   `ft_split`: Splits a string into an array of strings based on a delimiter.
    *   `ft_strmapi`: Applies a function to each character of a string.
    *   `ft_striteri`: Applies a function to each character of a string with its index.
    *   `ft_lstnew`: Creates a new linked list node.
    *   `ft_lstadd_front`: Adds a node to the beginning of a linked list.
    *   `ft_lstsize`: Returns the size of a linked list.
    *   `ft_lstlast`: Returns the last node of a linked list.
    *   `ft_lstadd_back`: Adds a node to the end of a linked list.
    *   `ft_lstdelone`: Deletes a single node from a linked list.
    *   `ft_lstclear`: Deletes an entire linked list.
    *   `ft_lstiter`: Iterates through a linked list and applies a function to each node.
    *   `ft_lstmap`: Creates a new linked list by applying a function to each node of an existing list.

## Technology Stack

*   C programming language

## Prerequisites

*   A C compiler (e.g., `gcc`, `clang`).
*   A standard build environment (e.g., `make`).

## Installation Instructions

1.  Clone the repository:

    ```bash
    git clone https://github.com/Hamza-fl/libft.git
    cd libft
    ```

2.  Compile the library:

    ```bash
    make
    ```

This will create the static library `libft.a`.

## Usage Guide

To use `libft` in your project:

1.  Include the header file `libft.h` in your source code:

    ```c
    #include "libft.h"
    ```

2.  Compile your code with the `libft.a` library:

    ```bash
    gcc your_code.c -L. -lft -o your_program
    ```

    *   `-L.`:  Specifies that the library is in the current directory.
    *   `-lft`: Links the `libft` library.  Note the 'ft' after the 'l' means 'libft.a' without the 'lib' prefix and '.a' suffix.

**Example:**

```c
#include "libft.h"
#include <stdio.h>

int main() {
    char *str = ft_strdup("Hello, libft!");
    printf("%s\n", str);
    free(str); // Important to free memory allocated by ft_strdup
    return 0;
}
```

Compile:

```bash
gcc example.c -L. -lft -o example
```

Run:

```bash
./example
```
