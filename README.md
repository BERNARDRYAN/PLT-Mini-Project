# BeginnerLangCompiler

BeginnerLangCompiler is a simple compiler project for the BeginLang `.bgl`
language. It scans tokens, builds a parse tree, checks syntax/semantics, and
generates a Java file named `GeneratedProgram.java`.

## Important Run Setup

Before running the compiler, make sure the project run configuration uses these
settings:

```text
Arguments: samples/output.bgl
Working Directory: D:\CODE\BeginnerLangCompiler\src
```

If another user stores the project in a different location, the working
directory must point to that user's own `src` folder, for example:

```text
Working Directory: <your project path>\BeginnerLangCompiler\src
```

This is important because the compiler reads the `.bgl` file from the `samples`
folder and writes the generated output files into the working directory.

## How To Use

1. Choose one BeginLang sample file from:

```text
src\samples
```

Example files:

```text
Calculator.bgl
GradeChecker.bgl
MultiplicationTable.bgl
ShoppingBill.bgl
```

2. Copy the content of the `.bgl` file you want to compile.

3. Paste it into:

```text
src\samples\output.bgl
```

4. Run the compiler with:

```text
samples/output.bgl
```

as the program argument.

5. After running, the compiler will generate:

```text
src\GeneratedProgram.java
src\TokenList.txt
src\ParseTree.txt
```

## Generated Files

`GeneratedProgram.java`

This is the Java program generated from `samples/output.bgl`. You can run this
file to test the compiled BeginLang program.

`TokenList.txt`

This file stores the scanner result. It shows each token and its token word.

`ParseTree.txt`

This file stores the parse tree result for the BeginLang program.

The token list and parse tree are also printed in the terminal when the compiler
runs.

## Complete Java Samples

The folder:

```text
src\programs
```

contains complete Java sample programs. These files can be run separately
without using the compiler.

Examples:

```text
Calculator.java
GradeChecker.java
MultiplicationTable.java
ShoppingBill.java
```

These Java files are useful for showing what the generated programs should look
like and how each sample works.

## Project Folders

```text
src\compiler
```

Contains the compiler source code, including the scanner, parser, semantic
analyzer, code generator, token list output, and parse tree output.

```text
src\samples
```

Contains BeginLang `.bgl` sample programs. Use `output.bgl` as the main input
file for compilation.

```text
src\programs
```

Contains complete Java versions of the sample programs.

## Notes

- Always set the working directory to the `src` folder.
- Always use `samples/output.bgl` as the argument.
- To compile a different BeginLang program, copy that program into
  `src\samples\output.bgl`, then run the compiler again.
- `GeneratedProgram.java`, `TokenList.txt`, and `ParseTree.txt` are regenerated
  every time the compiler runs.
