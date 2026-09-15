# Java Material

Study notes for Java fundamentals, written as Jupyter notebooks. Seven notebooks covering
syntax and variables, control flow, loops, arrays and ArrayLists, strings, and classes
and objects.

These are reference notes rather than a project. Each topic is built up the same way —
the concept in prose, the syntax as a reusable template, then a concrete example — so you
can come back and look things up.

---

## Java in Jupyter

The notebooks run on the **IJava** kernel against **JDK 21**, so Java executes cell by
cell the way Python would. That changes what the code looks like in a few places:

- Statements can appear at the top level without being wrapped in a class and a `main`
  method.
- `java.util` is available without an explicit import.

Code meant for a real `.java` file still needs the class wrapper and the imports, which
the notebooks show in the syntax templates even where the kernel doesn't require them.

---

## How the notebooks are written

1. **Concept** — what the construct is and when to use it, often with a comparison table
   of the options.
2. **Syntax** — a template using placeholder names like `datatype`, `var_name`, and
   `class_name`. These show the shape of the construct and are not meant to execute.
3. **Example** — real code, usually with output kept inline.

Because of step 2, "Run All" won't work cleanly. Read them, or run the example cells
selectively.

Several notebooks compare Java against Python directly, which is useful if Python came
first — the array-versus-list table in particular lays out static versus dynamic sizing,
single versus mixed types, and built-in methods versus the `Arrays` utility class.

---

## Contents

Roughly in the order they build on each other.

### Java- Basic

The foundation. Single-line and block comments; the class-plus-`main` structure every
Java program needs; `print()` versus `println()`; the primitive types with their ranges;
variable naming conventions; declaration and assignment, separately and combined; the
`final` keyword.

Then variable manipulation: arithmetic, comparison operators, compound assignment,
increment and decrement, string concatenation, and — importantly — why `==` is not how
you compare strings.

### Java-Control Flow

Logical statements and the three logical operators. `if`, `if`/`else`, `else if` chains,
and nested conditionals, each with a syntax template and a description of which branch
runs when. Closes with the `switch` statement as the alternative to a long `else if`
chain, including `break` and `default`.

### Java- Loop

`while` loops and the incrementing pattern that keeps them terminating. `for` loops.
Iterating over arrays and ArrayLists by index. `break` and `continue`. The enhanced
for-each loop as the cleaner option when you don't need the index.

### Java- Array

Arrays as fixed-size, single-type objects. Declaring and initializing in one line or
separately; indexing from zero and what `ArrayIndexOutOfBoundsException` means; creating
an empty array with `new` at a fixed size, then filling it; the `length` field.

Closes with the `java.util.Arrays` utility class — why arrays have no built-in methods of
their own, the import, a table of the class's static methods, and the practical
demonstration that printing an array directly gives you a memory reference while
`Arrays.toString()` gives you the contents.

### Java- ArrayList

The resizable counterpart. Importing `java.util.ArrayList`, a table of the available
methods, and then the operations one at a time: creating an empty list, `add()`,
`size()`, `get()`, `set()`, `remove()`, and `indexOf()`.

### Java-String

Strings as objects, and the three string classes distinguished up front — `String`
(immutable), `StringBuilder` (mutable), and `StringBuffer` (mutable and thread-safe).

Then the `String` methods worked one at a time: `length()`, `concat()`, `equals()`,
`indexOf()`, `charAt()`, `substring()`, and `toUpperCase()` / `toLowerCase()`, followed
by sections on `StringBuilder` and `StringBuffer`.

### Java-Classes and Objects

The longest notebook, and the one that pulls the rest together. A savings account is used
as the running analogy for what a class is before any code appears.

Covers declaring a class and its access modifiers; instantiating with `new`; constructors
and why the name must match the class; instance fields and the three ways to set them;
constructors with parameters; constructor overloading and how the compiler picks between
them by signature; what happens when you define no constructor at all.

Then methods: visibility modifiers, additional modifiers (`final`, `static`, `abstract`,
`transient`), return types, and calling methods on an object. Finishes with scope — why a
variable declared inside a method can't be reached from `main`, while an instance field
can — modifying attributes through methods, the `return` statement, and overriding
`toString()` so printing an object gives something readable instead of a memory address.

---

## Running the notebooks

You'll need a JDK (21 or later) and the [IJava](https://github.com/SpencerPark/IJava)
kernel installed alongside Jupyter:

```bash
jupyter notebook
```

Then pick the **Java** kernel when opening a notebook. To read them without running
anything, GitHub renders `.ipynb` files directly in the browser.
