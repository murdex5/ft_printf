<h1 align="center">
  ft_printf
</h1>

<p align="center">
  <em>A custom implementation of the C standard library function <code>printf</code>.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Language-C-blue.svg?style=for-the-badge" alt="Language C">
  <img src="https://img.shields.io/badge/School-42-black.svg?style=for-the-badge" alt="42 School Project">
</p>

## 📖 Table of Contents
- [About The Project](#-about-the-project)
- [Supported Specifiers](#-supported-specifiers)
- [How To Use](#-how-to-use)
- [Example](#-example)
- [Author](#-author)

## 📝 About The Project

`ft_printf` is a project from the 42 curriculum that challenges students to recreate the behavior of the standard C `printf` function. This project involves handling a variable number of arguments and formatting output based on type specifiers.

This implementation is written in C and handles some of the most common `printf` conversions. It's a lightweight and efficient alternative for projects where the full functionality of the standard `printf` is not required.

## ✨ Supported Specifiers

This version of `ft_printf` supports the following format specifiers:

| Specifier | Description                               |
| :-------: | ----------------------------------------- |
|    `%c`   | Prints a single character.                |
|    `%s`   | Prints a string of characters.            |
|    `%p`   | Prints a pointer address in hexadecimal.  |
|    `%d`   | Prints a signed decimal integer.          |
|    `%i`   | Prints a signed integer in base 10.       |
|    `%u`   | Prints an unsigned decimal integer.       |
|    `%x`   | Prints a number in hexadecimal (lowercase).|
|    `%X`   | Prints a number in hexadecimal (uppercase).|
|    `%%`   | Prints a literal percent sign.            |

## 🚀 How To Use

To use this `ft_printf` implementation in your own C project:

1.  **Add the files**: Copy all the `.c` source files and the `ft_printf.h` header file into your project directory.

2.  **Include the header**: In the file where you want to use `ft_printf`, include the header:
    ```c
    #include "ft_printf.h"
    ```

3.  **Compile**: Compile your project, including all the provided `.c` files. If you are using a `Makefile`, add the source files to your `SRCS` variable. For example:
    ```makefile
    SRCS = your_main.c ft_printf.c printf_utils.c utils0.c utils1.c utils2.c utils3.c utils4.c
    ```
    Then, run `make`.

## 💡 Example

Here is a simple example of how to use `ft_printf`:

```c
#include "ft_printf.h"

int main(void)
{
    char *str = "world";
    int   num = -42;
    unsigned int hex = 3735928559; // 0xdeadbeef

    ft_printf("Hello, %s!\n", str);
    ft_printf("The number is: %d\n", num);
    ft_printf("A pointer address: %p\n", str);
    ft_printf("Hex (lowercase): %x\n", hex);
    ft_printf("Hex (uppercase): %X\n", hex);
    ft_printf("Printing a single char: %c\n", 'A');
    ft_printf("Don't forget the percent sign: %%\n");

    return (0);
}
```

**Expected Output:**
```
Hello, world!
The number is: -42
A pointer address: 0x10...
Hex (lowercase): deadbeef
Hex (uppercase): DEADBEEF
Printing a single char: A
Don't forget the percent sign: %
```

## ✍️ Author

**kadferna** - [GitHub Profile](https://github.com/murdex5)