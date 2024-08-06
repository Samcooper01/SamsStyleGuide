# Sam's Style Guide

## Purpose

The software development work in these repositories is for learning purposes. These projects are intended for personal enjoyment and educational growth. The purpose of this document is to define the boundaries to maximize enjoyment from these projects while also minimizing bugs and achieving a satisfactory level of code readability so others can understand the functionality of the code.

## Sam's Guiding Principles

1. **Minimize Bugs:** Code should prioritize minimizing bugs. It should be written in a way that allows a compiler/linker to detect problems before execution.
2. **Simplicity and Clarity:** Code should be simple in nature and free from ambiguity that could be interpreted differently at runtime by different compilers or even readers.
3. **Readability and Reliability:** Readability and reliability are of equal importance to programmer convenience.
4. **Consistency Across Projects:** Code style should not be specific to project type. This guide should be applicable to all project types.

## C Program Principles

*These are taken directly from the Barr C Coding Standard.*

- **Avoid Altering Keywords:** The preprocessor directive `#define` shall not be used to alter or rename any keyword or other aspect of the programming language.
- **Line Width:** The width of all lines in a program shall be limited to a maximum of 80 characters.
- **Single Line Statements:** Single line statements without braces may be used.
- **Brace Placement:** Braces should be placed below the title they open.
- **Function Structure:** Functions should follow this structure:
  ```c
  <RET TYPE>
  function_name(
      <PARAMETER>,
      <PARAMETER>,
      <PARAMETER>
  )
  {
      FUNCTION BODY

      <SINGLE EXIT POINT>
  }

- **Single Exit Point:** Functions should mostly exit from one point.
- **Function Length:** Functions should be no longer than 100 lines.
- **Operator Rules:** Avoid relying on operator precedence rules; use parentheses for clarity.
- **Avoid Abbreviations:** Avoid abbreviations. Use longer variable names if necessary for clarity.
- **Keyword Usage:** Avoid using uncommon keywords (e.g., goto, register, auto).
- **Avoid 'continue':** Try to avoid the use of the continue statement.
- **Use const:** Use const where applicable.
- **Use static:** Use static for functions not visible outside the file (private functions).
- **File Purpose:** Each file should have a specific purpose described by its name.
- **Function Purpose:** Each function should have a specific purpose described by its name and comments.
- **Avoid Complexity:** Avoid complex one-liners. Use multiple lines for clarity, with each line performing one assignment or arithmetic operation.
- **for Statement Formatting:** Each semicolon separating the elements of a for statement shall be followed by one space.
- **Pointer Formatting:** * and & should not have a space on the operand side.
- **Unary Operator Formatting:** Unary operators should not have a space on the operand side.
- **Preprocessor Alignment:** Preprocessor statements should be visually aligned as follows:
  ```c
  #ifdef USE_UNICODE_STRINGS
  #   define BUFFER_BYTES 128
  #else
  #   define BUFFER_BYTES 64
  #endif

- **End-of-File Comment:** Each source file should end with a comment marking the end of the file:
  ```c
  /* End of file: NAME.c */
- **Blank Lines:** Each natural block of code should have a blank line before and after.
- **Header Files:** All header files should use include guards
  ```c
  #ifndef ADC_H
  #define ADC_H
  ...
  #endif /* ADC_H */
- **Header File Content:** The header file shall only identify procedures, constants, and data types necessary for other modules to be informed about (via prototypes, macros, #define, and typedefs).
- **Source File Order:** Source files should be organized as follows:
  1. Comment Block
  2. Include statements
  3. Macros
  4. typedefs + structs + unions
  5. Static data
  6. Function bodies
  7. End-of-file comment
- **No Source File Inclusion:** No source file shall #include another source file.
- **Avoid Floating Points:** Avoid floating point operations where possible.
- **Variable Names:** Variable names should be at least 3 characters long. Loop counter variables should also follow this rule if possible.
- **Constant Placement:** When evaluating equivalence, place the constant on the left side:
  ```c
  if (NULL == var_name) {
    // Code
  }

## Comments Guidelines

- **Function Documentation:** Every function that can't describe what it is doing from the caller name alone should have a comment section.
Note: All sections are optional depending on the function's complexity.

- **Function Header:** Function headers should go above the function declaration, preferably in a header file.
```c
/**
 * @brief [Brief description of the function's purpose]
 *
 * @param [param1] [Description of the first parameter]
 * @param [param2] [Description of the second parameter]
 * 
 * @return [Description of what the function returns]
 */
```

- **File Header:** Each file, including the main file, should have a header like so:

```c
/*
 * Program Name: [Name of the program]
 * Description: [Short description of what the program does]
 * Author: [Your Name]
 *
 * Dependencies: [List of dependencies]
 * Compilation: [Instructions on how to compile]
 * Usage: [Instructions on how to use the program]
 *
 * Notes:
 *      None.
 * 
 * Style:
 *  https://github.com/Samcooper01/StyleGuide/tree/main
 */
```

## Conclusion
These guidelines and principles are intended to create a structured and consistent coding style that promotes readability, reliability, and maintainability. By following these standards, we aim to minimize bugs and enhance the enjoyment of developing software in these repositories.
