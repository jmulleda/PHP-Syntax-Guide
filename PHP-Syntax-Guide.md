# PHP Syntax Guide
### Jonathan Mulleda
## How to make comments
- Use double forward slashes for single line
- Use forward slash and asterisk for multiple lines
```
// Single line comment
/* Multiple line comment */
```
## How to define Variables 

Variable names ...
- Are case sensitive.
- Must start with a letter or an underscore, and cannot start with a number
- Can only contain alpha-numerica characters and underscores.
- Cannot contain spaces.
```
<?php
    $sampleVariable = "Variable Value";
    $course = "Web-107";
    $term = "Winter Semester";
?>
```
## The Echo & Print Statements
- Echo and print are both used to output data to the screen
- Echo can accept multiple parameters, and has no return value.  Echo is faster than print.
- Print can only accept one argument, and has a return value of 1.
## Echo 
```
<?php
    $sampleVariable = "Hello World!";
    echo $sampleVariable;
    echo "This is a string.";
    echo "<p>HTML tag</p>"
?>
```
## Print
```
<?php
    $sampleVariable = "Hello universe!";
    print $sampleVariable;
    print "This outputs a string too.";
    print "<p>HTML tag</p>";
?>
```
## Data Types 
Data types in PHP include:
- Integers
- Strings
- Floating point
- Booleans
- Arrays
- Resources
## Integers
- Integers are non-decimal whole numbers which can be in decimal, hexadecimal, or octal.
```
<?php
   echo 98765;
?>
```
## Strings
- Strings are characters enclosed in single (' ') or double (" ") quotes.
```
<?php
    echo "I am a string.";
?>
```
## Floating
- A floating point number is a number in exponential form, or a number with a decimal point
```
<?php
    $pi = 3.141592653589793238462643;
    echo $pi;
?>
```
## Booleans
- Booleans are true or false statements where 1 = true and 0 = false.
```
<?php
    $legalAge = true;
?>
```
## Arrays
- Arrays are variables that hold several values.
```
<?php
    $students = array("Jonathan", "Lisa", "Benton", "Aimee", "Marty");
    echo $students;
?>
```
## Resources
- A resource references an external source such as a database. 
```
<?php
// Verify database connection
$conn = new PDO("mysql:host=$servername;dbname=library", $username, $password);
$conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
echo "Connected successfully!";
?>
```
## Strings

- Strings in single quotations (' ') are unable to process special characters, making it impossible to interpret the dollar sign ($) sign at the beginning of the variable name.  
```
<?php
    $user = 'Jonathan';
    echo 'Hello $user!'; 
    // OUTPUT: "Hello $user!"
?>
```
- Double quoted strings (" ") can interpret variables and can also recognize special characters
```
<?php
    $user = "Jonathan";
    echo "Hello $user!";
    // OUTPUT: "Hello Jonathan!"
?>
```
## Numbers
## Integers
- Integers are non-decimal whole numbers which can be in decimal, hexadecimal, or octal.
### Tips for Integer 
- Must contain at least one digit
- Cannot contain decimal points
- Can be either positive or negative
- Can be in decimal, hexadecimal, or octal format
## Floating Point Numbers (Floats/Doubles)
- Floating point numbers are numbers in exponential form or numbers with a decimal point.
## Constants
- A constant cannot be changed and are globally scoped.
- Constant names must begin with a letter or underscore, no $ is required at the beginning of the name.
```
<?php
    define("city", "Vancouver");
    echo city; 
    // OUTPUT "Vancouver"
?>
```
## Operators
### Arithmetic Operators

- Arithmetic Operators can perform arithmetic operations with numeric values.

| Operator 	| Name           	| Example  	|
|----------	|----------------	|-----------|
| +        	| Addition       	| $x + $y  	|
| -        	| Subtraction    	| $x - $y  	|
| *        	| Multiplication 	| $x * $y  	|
| /        	| Division       	| $y / $x  	|
| %        	| Modulo         	| $y % $x  	|
| **       	| Exponentiation 	| $y ** $x 	|

### Assignment Operators

- Assignment Operators are used to write values to variables.

| Assignment 	| Same as   	|
|------------	|-----------	|
| a += b     	| a = a + b 	|
| a -= b     	| a = a - b 	|
| a *= b     	| a = a * b 	|
| a /= b     	| a = a / b 	|
| a %= b     	| a = a % b 	|

### Comparison Operators

- Comparison Operators are used to compare two values.

| Operator 	| Name                                 	|
|----------	|--------------------------------------	|
| ==       	| Equal                                	|
| ===      	| Not Equal                            	|
| !=       	| Not Identical                        	|
| <>       	| Less Than                            	|
| !==      	| Greater Than                         	|
| <        	| Less Than                            	|
| >        	| Greater Than                         	|
| <=       	| Less Than or Equal To                	|
| >=       	| Greater Than or Equal To             	|
| <=>      	| Less Than, Equal To, or Greater Than 	|

### Logical Operators

- Logical Operators are used to combine conditional statements.

| Operator 	| Name                                 	|
|----------	|--------------------------------------	|
| and      	| And                                	|
| or      	| Or                            	    |
| xor      	| Exclusive Or                        	|
| !       	| Not                                  	|
| &&      	| And                                  	|
| ||       	| Or                                	|

### Increment/Decrement Operators 

- Increment/decrement operators are used to increment/decrement a variables value.

| Operator 	| Description                                 	|
|----------	|--------------------------------------	|
| ++$a      | Increments a variable by one, then returns it                                	|
| $a++     	| Returns a variable, then increments it by one                            	    |
| --$a     	| Decrements the variable by one, returns it afterward                         	|
| $a--     	| Returns the variable then decrements it by one                                   	|

### String Operators
| Operator 	| Description                                 	|
|----------	|--------------------------------------	|
| .      	| Used to concatenate arguments                                	|
| .=      	| Used to append the argument on the right to the left argument                            	    |

## If Statement

- Executes code if one condition is met.
```
    if (condition) {
    code to execute if condition is met
    } 

<?php
    if ($time > 0600) {
        echo "Have a wonderful day!";
    }
?>
```
### If ... Else
- Executes one piece of code if a condition is met, and different piece of code if not.

```
    if (condition) {
    code to execute if condition is met
    } else {
    code to execute if condition is not met
    } 

<?php
    if ($time < 1400) {
        echo "Good day!";
    } else {
        echo "Good night!";
    }
?>
```
### If ... Elseif ... Else

- Executes different code for more than two conditions.

```
    if (condition) {
         code to execute if condition is met
    } elseif (condition) {
         code to execute if this condition is met
    } else {
         code to execute if none of the conditions are met
    }

<?php
    if ($time < 1200) {
        echo "Good morning!";
    } elseif ($time < 1800) {
        echo "Good day!";
    } else {
        echo "Good night!";
    }
?>
```
## Functions
### Built In Functions
- PHP has built-in functions that can be called directly. 

### User-Defined Functions
- Creating user-defined functions can save a lot of time and effort by automating things.
### Creating a Function
```
<?php
function function_name(){
    executable code;
}
?>
```
### Function Parameters or Arguments
```
<?php
function function_name($first_parameter, $second_parameter) {
    executable code;
}
?>
```
## Arrays
- Arrays are variables that hold several values of a similar data type.

### Declaring an Array
```
<?php
    $students = array("Jonathan", "Lisa", "Benton", "Aimee", "Marty");
    $grades = array(90, 95, 98, 92, 96);
    echo $students;
    echo $grades;
?>    
```
## Loops
- Loops are used to execute the same code over and over again, if a certain condition has been met.
### While Loop
 - Loops through a block of code if condition is met
```
while (condition that must apply) {
 // code to execute goes here
} 

<?php
    $index = 1;
    while ($index <= 10) {
        echo $index;
        $index++;
    }
?>
```
### Do ... While Loop

- The block of code is executed once before the condition is evaluated.  If the condition is met, the statement repeats forever as long as the condition stays true.
```
do {
 // code to execute goes here;
} while (condition that must apply); 

<?php
    $index = 1;
    do {
        echo $index;
        $i++;
    } while ($i <= 10);
?>
```
### For Loop
- Loops through a block of code until the counter reaches a specified number.

```
for (starting counter value; ending counter value; increment by which
to increase) {
 // code to execute goes here
} 
<?php
    for ($i = 0; $x <= 10; $i++) {
        echo "$x <br>";
    }
?>
```
### Foreach Loop

Loops through a block of code once for each element within an array.

```
foreach ($InsertYourArrayName as $value) {
 // code to execute goes here 
}

<?php
    $students = array("Jonathan", "Lisa", "Benton", "Aimee", "Marty");
    foreach ($students as $student) {
        echo "$student <br>";
    }
?>
```