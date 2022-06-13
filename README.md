# Lab 1: Setup


## 0. Intro

The purpose of this lab is twofold: to help you get set up with working on CS123 projects locally, and to help you learn the basics of C++ -- The programming language that we will be using for the labs and the assignments.

In the rest of this 1-2h lab, you will:

1. Install Qt 6 locally on your computer, and
2. Build and run a starter Qt program, and
3. ??placeholder for C++ tutorial

**Note:** Overall Qt 6 and the C++ compiler will suck up ??GB of space, approximately. Additional images or scene files can also take up a fair bit of space. Be sure you have room.

##
##
## Installing Qt 6

## **Windows**

1. Install Qt (takes about ?? mins)

    a. [https://www.qt.io/download-qt-installer](https://www.qt.io/download-qt-installer)

    b. Open when done downloading
2. Follow instructions on the installer to create a new Qt account if you do not have one
3. When selecting components:

    a. Choose “Custom Installation”
![](1.png)

    b. Under “Qt”, you’ll need Qt 6.2.4, and select the items as shown in the screenshot for the “Developer and Designer Tools” section. MinGW is what provides the GCC compiler you'll need to compile your C++ code.
![](2.png)
4. Continue and finish the installation process.
5. We'll provide an example on how to open, configure and run a Qt project later on in this guide.

## Placeholders

## Hello World
A simple C++ program that does nothing is provided below:

```cpp
// A C++ program always starts from the main() function
// main() returns an integer indicating the execution state of the program
auto main()->int {
    // you may leave the function body of main() empty if it does nothing
    // the compiler automatically inserts "return 0;" for you
    // indicating the execution is successful
}
```

In a similar way that Python uses `import`s, C++ uses `#include`s. The imported functionalities are normally grouped under a namespace, which is denoted with the double colon `::` symbol. We'll use the C++ Standard Library namespace, also known as _std_, for our Hello World program

The **input/output library** (`iostream` library) is part of the C++ standard library that deals with basic input and output. We'll use the functionality in this library to get input from the keyboard and output data to the console. The _io_ part of _iostream_ stands for _input/output_.

- Available any time via `#include <iostream>`
- `std::cout` is how you will print to the command line
  - i.e. the output window in QtCreator, your IDE for this course :)
- `<<` inserts characters into the current output stream
- Works like string concatenation where the stream is the output string
- `std::endl` ends the line and inserts a newline character
- `std::cin` and `std::cerr` also exist
  - `std::cin` reads from stdin (terminal input)
  - `std::cerr` prints to stderr (terminal error messages)

#### ***Task 1:***

We are ready to write something on the screen!

- Write "Hello World!" in a `std::cout << "" << std::endl;` call in the `main` function.

At this point when you run your program you should see "Hello World!"

Now we can get into the more fun stuff!

## Primitive Types, Variables and Functions

Like many other programming languages, C++ comes with several primitive types including:

- integer-like types (integers, booleans, characters)
- floating point types
- arrays
- functions and lambdas
- pointers and references

Some of these you might already know from languages you learned before, some, such as pointers and references, are C++ concepts which we'll expand in the following sections. It is also worth noting that strings are not a primitive type in C++, string literals are simply character arrays. However, the standard library does provide the `std::string` type which allows us to perform common string operations.

C++ is a _typed_ language, meaning that we either have to declare the type when creating a variable:

```cpp
int x = 42;
double y = 3.14;
```

or use `auto` to tell the compiler to deduce the type for us from the initialization. This could be useful if the type name is very long or if we know roughly about what something is, but we're not sure about the exact type.

```cpp
auto z = 2.71; // type of z deduced as double

// I'm not exactly sure about the type of a string literal.
// but I can ask the compiler to deduce it for me using auto
auto w = "random string abcd";
```