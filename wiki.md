hello this is art, I decided to dive deeper into the C language at 31-10-2026, and in order to better memorize my studies i thought that its best to write it down
Important Info about Syntax:
#include - is a directive that takes contents of a file and places it in the output which is then handed to the C compiler.
stdio.h - is a header allowing usage of standard functions, like printf and other stuff
int main(){} - is the entry point of a C program. at the end returns 0 if success, or 1 if failed
{} - are code blocks for int main and void functions and other

Pointers:
Pointers - are variables that point to a memory address of another variable.
After making a pointer, its now possible to get the value stored in a certain memory address, which the
pointer holds. This is done by the Dereference operator (*):
  printf("%p", ptr); // Outputs the memory address
  printf("%d", *ptr); // Outputs the value of a variable with the dereference operator
Dereference can also be used to change the value of a variable:
  *ptr = 50 (use the dereference oper. and change the stored value in there)
In order to declare a pointer variable:
  int myAge = 50;
  int* ptr = &myAge // (*) is used to define it as a pointer, (&) is used to get the memory address and assign it to the pointer

Format Specifiers:
%c - characters, single or array
%d - signed integer
%f - for floats
%i - signed integer (both %i and %d works i think)
%lf - for a double type
%s - for string
%% - prints % character since % already acts as a specifier
%n - prints a blank space, useful for proper texts

Arithmetic Operators in C:
++ / Increment / increases value of a variable by 1 (written like ++variable in a line of code, strange ik)
-- / Decrement / decreases value of a variable by 1 (written same as above)
% / Modulus / returns the remainder of a division

Logical Operators in C:
&& / AND / x > 3 && x < 10 -- returns 1 if both statements are true
|| / OR / x > 3 || x < 4 -- returns 1 if one of the statements is true
! / NOT / !(x > 3 && x < 10) / reverses the result, returns 0 if it was 1

Info regarding printing:
1. you can print values directly in printf without storing them in variables:
	#printf("My favorite number is: %d", 15);
2. you can limit the amount of zeros in a decimal:
   int lol = 3.5
   printf("%.2f", lol)
so this will print: 3.50, because you limited the decimals to 2 only. if you put 100 into the limiter it will print out 100 decimals

Info regarding math operators, math and integers in general:
1. math operations with variables are simple as in Lua, you can just have 2 int variables holding 5 and 10,
then add them up in a separate variable
   int x = 5;
   int y = 10;
   int sum = x + y;
updating an existing variable is also possible, same as before:
   int x = 5;
   x = x + 1;
2. its possible to declare multiple values into a single variable, such as declaring 3 separate integers into a single int variable
   int x = 2, y = 3, z = 4
however all variables must be of same type in a single variable

3. characters are stored as numbers because of ASCII values. example: A = 65, B = 66 and so on. so if you print a char with %d instead of %c it will print its ASCII value

4. whole integers and floats are loyal to their kind: if you try to divide whole integers for example 5/2, the result will be 2 despite the correct being 2.5. this is because Int type only contain whole numbers, and for decimals you need float. If for example you want to put the result of 5/2 in a variable,
youll need to do Explicit Conversion, manually convert the result to a certain type.
   float result = (float) 5 / 2  -- (2.5000000)
Explicit Conversion - manual conversion of types by the user
Implicit Converison - automatic conversion of types by compiler, e.g. when assigning an int value to a float type.
   float myFloat = 9; (this will print 9.000000 because of float type influencing int)

Info regarding booleans:
1. Booleans can only be accessed by including a header file <stdbool.h>
2. Is declared by: bool isCodingFun = true;
3. booleans are only returned as 1(true) or 0(false). therefore &d can be used to print a bool.

Signed and Unsigned Integers:
Signed can store both positive and negative values (-1 and below, 0 and above)
Unsigned cannot store non-negative values (0 and up)

How to do For Loops:
> for (statement1, statement2; statement3) {
  // code goes here
} 
  Statement 1 - is executed only a SINGLE time before the execution of the code block
  Statement 2 - defines the condition for executing the code block
  Statement 3 - is executed everytime after the code block has been executed
