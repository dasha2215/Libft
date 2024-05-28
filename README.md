# Libft

## Overview

Libft is a custom C library that implements a variety of standard functions found in the C standard library, as well as some additional utility functions. This library is designed to be a foundational tool for future C projects, providing a consistent and reliable set of functions for common tasks.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Functions](#functions)
  - [Libc Functions](#libc-functions)
  - [Additional Functions](#additional-functions)
- [License](#license)

## Introduction

C programming can be challenging without access to highly useful standard functions. Libft is a project aimed at understanding and implementing these functions from scratch. This library will be helpful for various C school assignments and future projects.

## Features

- Implementation of essential libc functions
- Additional utility functions
- Comprehensive Makefile for building the library
- Adherence to strict coding standards and norms

## Installation

To use the libft library in your projects, follow these steps:

1. Clone the repository:

```sh
git clone https://github.com/dasha2215/libft.git
cd libft
```
2. Compile the library using the provided Makefile:

  ```sh
  make
  ```
3. Include the libft.h header in your project and link the compiled library:

  ```c
  #include "libft.h"
  ```
4. Use the following command to compile your project with the libft library:

  ```sh
  cc -o my_program my_program.c -L. -lft
  ```

## Usage
Libft provides a wide range of functions for string manipulation, memory management, and more. Below is a brief overview of the functions included in the library.

## Functions

### Libc Functions

The following functions have been reimplemented to match their counterparts in the standard C library:

- **Character Manipulation Functions**
  - `int ft_isalpha(int c)`
  - `int ft_isdigit(int c)`
  - `int ft_isalnum(int c)`
  - `int ft_isascii(int c)`
  - `int ft_isprint(int c)`
  - `int ft_toupper(int c)`
  - `int ft_tolower(int c)`

- **String Manipulation Functions**
  - `size_t ft_strlen(const char *s)`
  - `char *ft_strdup(const char *s1)`
  - `char *ft_strchr(const char *s, int c)`
  - `char *ft_strrchr(const char *s, int c)`
  - `int ft_strcmp(const char *s1, const char *s2)`
  - `int ft_strncmp(const char *s1, const char *s2, size_t n)`
  - `char *ft_strnstr(const char *haystack, const char *needle, size_t len)`
  - `size_t ft_strlcpy(char *dst, const char *src, size_t dstsize)`
  - `size_t ft_strlcat(char *dst, const char *src, size_t dstsize)`

- **Memory Manipulation Functions**
  - `void *ft_memset(void *b, int c, size_t len)`
  - `void ft_bzero(void *s, size_t n)`
  - `void *ft_memcpy(void *dst, const void *src, size_t n)`
  - `void *ft_memmove(void *dst, const void *src, size_t len)`
  - `void *ft_memchr(const void *s, int c, size_t n)`
  - `int ft_memcmp(const void *s1, const void *s2, size_t n)`

- **Conversion Functions**
  - `int ft_atoi(const char *str)`
  - `char *ft_itoa(int n)`

- **Utility Functions**
  - `void *ft_calloc(size_t count, size_t size)`

### Additional Functions

In addition to the standard libc functions, the library includes the following utility functions:

- **String Manipulation Functions**
  - `char *ft_substr(char const *s, unsigned int start, size_t len)`
    - Creates a substring from a given string, starting at a specified index up to a certain length.
  - `char *ft_strjoin(char const *s1, char const *s2)`
    - Concatenates two strings into a new string, allocated with `malloc`.
  - `char *ft_strtrim(char const *s1, char const *set)`
    - Trims the beginning and end of a string based on a set of characters to remove.
  - `char **ft_split(char const *s, char c)`
    - Splits a string into an array of strings using a delimiter character.
  - `char *ft_strmapi(char const *s, char (*f)(unsigned int, char))`
    - Applies a function to each character of a string, creating a new string with the results.
  - `void ft_striteri(char *s, void (*f)(unsigned int, char*))`
    - Applies a function to each character of a string, with the character's index passed as an argument.

- **Output Functions**
  - `void ft_putchar_fd(char c, int fd)`
    - Outputs a character to a file descriptor.
  - `void ft_putstr_fd(char *s, int fd)`
    - Outputs a string to a file descriptor.
  - `void ft_putendl_fd(char *s, int fd)`
    - Outputs a string followed by a newline to a file descriptor.
  - `void ft_putnbr_fd(int n, int fd)`
    - Outputs an integer to a file descriptor.

- **List Manipulation Functions**
  - `t_list *ft_lstnew(void *content)`
    - Creates a new list node with given content.
  - `void ft_lstadd_front(t_list **lst, t_list *new)`
    - Adds a new node at the beginning of a list.
  - `int ft_lstsize(t_list *lst)`
    - Counts the elements in a list.
  - `t_list *ft_lstlast(t_list *lst)`
    - Finds the last node of a list.
  - `void ft_lstadd_back(t_list **lst, t_list *new)`
    - Adds a new node at the end of a list.
  - `void ft_lstdelone(t_list *lst, void (*del)(void*))`
    - Frees a node and its content using a given function.
  - `void ft_lstclear(t_list **lst, void (*del)(void*))`
    - Deletes and frees a node and all successors.
  - `void ft_lstiter(t_list *lst, void (*f)(void *))`
    - Iterates the list and applies the function to each node's content.
  - `t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *))`
    - Iterates the list, applies the function to each node's content, and creates a new list with the results.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
