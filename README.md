# newt-calculator

An interactive calculator written in **Newt**.

This is a small example program for the Newt scripting language. It asks for two numbers, then prints the result of:

- addition
- subtraction
- multiplication
- division

## Example Run

```txt
Newt Calculator
a: 50
b: 50
100
0
2500
1
```

## Files

```txt
interactive_calculator.nt   # the Newt calculator script
run.sh                      # helper script to run the calculator
```

## Requirements

This project expects the main Newt repo to be next to this folder:

```txt
projects/
  newt/
    newt.exe
  newt-calculator/
    interactive_calculator.nt
    run.sh
```

Build Newt from the main `newt` repo first:

```sh
cd ../newt
gcc -std=c11 -Wall -Wextra -pedantic -o newt.exe src/main.c
```

Then return to this repo:

```sh
cd ../newt-calculator
```

## Run

```sh
./run.sh
```

The runner calls:

```sh
../newt/newt.exe --run interactive_calculator.nt
```

## Calculator Source

```newt
print "Newt Calculator"

val a = input_number("a: ")
val b = input_number("b: ")

print a + b
print a - b
print a * b
print a / b
```

## About Newt

Newt is a small experimental scripting language built in C.

Newt was created by **drgropp**.
