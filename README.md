# linux-variable
 Variables are fundamental to programming and scripting in Linux, allowing users to store values such as strings, numbers, and commands for later use.
  Variables are used to store values and can be referenced later in the script. To assign a value to a variable, use the syntax varname=value.
 # Naming Rules:
Variable names must begin with a letter (A-Z or a-z) or an underscore (_).
They can contain letters, numbers (0-9), and underscores but cannot start with a digit or include spaces or special characters (except underscores)
# Defining Variables:
Variables are defined using the equals sign (=). For example:
NAME="Sabiya"
AGE=23
Note..>that there should be no spaces around the equals sign 
# Accessing Values:
To retrieve the value stored in a variable, prefix the variable name with a dollar sign ($). For example:
echo $NAME
This command will output "sabiya" if the variable NAME is defined as above 
# math fuctions
To perform mathematical functions in Bash, you can use several methods, each suited for different types of calculations. Here’s a concise guide on how to do math in Bash:
1. Arithmetic Expansion
The most common way to perform arithmetic operations is using the $(( )) syntax. This allows you to execute basic arithmetic operations such as addition, subtraction, multiplication, and division.
Example:
bash
# Addition
result=$((5 + 3))
echo $result  # Output: 8

# Subtraction
result=$((10 - 2))
echo $result  # Output: 8

# Multiplication
result=$((4 * 2))
echo $result  # Output: 8

# Division
result=$((20 / 4))
echo $result  # Output: 5
# Using let Command
The let command is another way to perform arithmetic operations without needing the dollar sign or parentheses.
Example:

let result=10*20
echo $result  # Output: 200
# Using bc for Floating Point Arithmetic
For more complex calculations, especially those involving floating-point numbers, you can use the bc command. This command supports arbitrary precision and allows for more advanced mathematical functions.
Example:

result=$(echo "scale=2; 10 / 3" | bc)
echo $result  # Output: 3.33
In this example, scale=2 sets the number of decimal places.
#  Using expr Command
The expr command can also be used for basic arithmetic but requires spaces around operators.
# Example:
a=10
b=3
sum=$(expr $a + $b)
echo $sum   # Output: 13

sub=$(expr $a - $b)
echo $sub   # Output: 7

mul=$(expr $a \* $b)
echo $mul   # Output: 30

div=$(expr $a / $b)
echo $div   # Output: 3
Summary of Operators:
Addition: +
Subtraction: -
Multiplication: *
Division: /
Modulus: %
# Conclusion
Bash provides multiple methods for performing mathematical operations, from simple integer arithmetic using $(( )) to more complex calculations with bc. Depending on your needs—whether you're working with integers or floating-point numbers—you can choose the appropriate method to achieve your desired results.
