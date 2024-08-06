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
