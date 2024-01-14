# commands
command -v = check if a command is available is system 
echo = print
read = input
the > symbol write the output of a command to a file
the >> append the output of a command to a file without overwrite it
the < pass the output to the command
echo $? = ask bash about previous command
echo "hello imran" | tr m n = replace all m letters with n letters
echo "hello imran" | sed 's/ /n/g' = replace all the space with n 
exit  0 = exit script with code 0
# math
expr 1 + 2 = to calcule it u need that expr


```
# Addition
result_add=$((5 + 3))
echo "Addition: $result_add"

# Subtraction
result_sub=$((10 - 4))
echo "Subtraction: $result_sub"

# Multiplication
result_mul=$((6 * 7))
echo "Multiplication: $result_mul"
( in terminal do :expr 10 \* 4)

# Division
result_div=$((20 / 4))
echo "Division: $result_div"

# Modulus (Remainder)
result_mod=$((15 % 4))
echo "Modulus: $result_mod"
```

# functions
## If Statements
In Bash, `if` statements are used to conditionally execute a block of code based on the evaluation of a condition. The basic syntax of an `if` statement in Bash is as follows:

```
if [ condition ]; then
    # Code to be executed if the condition is true
else
    # Code to be executed if the condition is false
fi
```

Common comparison operators used in if statements include:

-eq: Equal to
-ne: Not equal to
-gt: Greater than
-lt: Less than
-ge: Greater than or equal to
-le: Less than or equal to

**example :**
```#!/bin/bash

# Example variable
number=10

# If statement
if [ $number -gt 5 ]; then
    echo "Greater than 5."
else
    echo "Not greater than 5."
fi

```

You can also use logical operators such as `&&` (logical AND) and `||` (logical OR) to combine multiple conditions. 

**example :** 
```#!/bin/bash

# Example variables
age=18
has_permission=true

# If statement with logical AND
if [ $age -ge 18 ] && [ $has_permission == true ]; then
    echo "You are eligible."
else
    echo "You are not eligible."
fi

```

### ! mark


In Bash, the exclamation mark (`!`) is used for negation. When you include it in an `if` statement, it negates the result of the condition. Here's a simple example:
```
#!/bin/bash

# Example variable
number=3

# If statement with negation (!)
if [ ! $number -gt 5 ]; then
    echo "Not greater than 5."
else
    echo "Greater than 5."
fi
```
In this example, it checks if the variable `number` is not greater than 5 and prints the corresponding message. The `!` negates the condition, so the code block after `then` is executed when the condition is false.
### -f
In Bash, the `-f` test operator is used to check whether a file exists and is a regular file (not a directory or a special file). When combined with an `if` statement, it allows you to conditionally execute code based on the existence and type of a file. Here's an example:
```
#!/bin/bash

# Example file path
file_path="/path/to/file.txt"

# If statement with -f test operator
if [ -f "$file_path" ]; then
    echo "The file exists and is a regular file."
else
    echo "The file does not exist or is not a regular file."
fi
```
 You can replace `"/path/to/file.txt"` with the actual path of the file you want to check. Adjust the code accordingly based on your specific requirements.
 ```
# check is certain file exist in folder
if [ -f /home/gojo/Documents/mycode/mastertheLS.sh ]; then
	echo "file exist"
else
	echo "file does not exist"
fi
```
### -d
In Bash, the `-d` test operator is used to check whether a given path exists and is a directory. When used in an `if` statement, it allows you to conditionally execute code based on the existence and type of a directory. Here's an example:
```#!/bin/bash
# Example directory path
directory_path="/home/gojo/folder"

# If statement with -d test operator
if [ -d "$directory_path" ]; then
    echo "The directory exists."
else
    echo "The directory does not exist or is not a directory."
fi
```

### exitcodes
In Bash, the exit code of a command or script is stored in `$?`. An exit code of 0 usually means success, while non-zero values indicate errors. You can check and act upon the exit code using an `if` statement:
```
command_that_might_fail
if [ $? -eq 0 ]; then
    echo "Success"
else
    echo "Failure"
fi
```
