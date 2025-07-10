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

1.  **Clone the repository and compile the library**: First, clone this repository to your local machine and run `make` to compile the source files into a static library archive called `libftprintf.a`.
    ```bash
    git clone https://github.com/murdex5/ft_printf.git
    cd ft_printf
    make
    ```

2.  **Include the library in your project**:
    *   Copy the `libftprintf.a` file and the `ft_printf.h` header file into your project's directory.
    *   In the C file where you want to use `ft_printf`, include the header:
        ```c
        #include "ft_printf.h"
        ```

3.  **Compile your project**: When compiling your project, you need to tell the compiler to link against the `ft_printf` library.
    
    For example, if you have a `main.c` file, you would compile it like this:
    ```bash
    gcc main.c -L. -lftprintf -o your_program_name
    ```
    *   `main.c` is your source file.
    *   `-L.` tells the linker to look for libraries in the current directory.
    *   `-lftprintf` tells the linker to link the `ft_printf` library. Note that `lib` and `.a` are omitted.
    *   `-o your_program_name` specifies the name of the output executable.

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