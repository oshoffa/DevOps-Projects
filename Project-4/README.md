# SHELL SCRIPTING HANDS-ON PROJECT 

# Introduction To Shell Scripting 

## Shell Scripting Syntax Element 

1. We assign values to variables using the = operator, and access their values using the variable name preceded by a $ sign. 

Example: Assigning value to a variable `name=John` 

Example: Retrieving value from a variable `echo $name` 

2. Control Flow: Words like if, elif or else are used for loop, and for loops and case statements are used to control the flow of execution. We make decisions, iterate over lists, and execute different commands with them.

Example: Using if, elif, else to execute script based on condition.

![Alt text](<Images/Screenshot (312).png>) 

Output: 

![Alt text](<Images/Screenshot (315).png>) 

Example: Iterating through a list using a for loop. 

![Alt text](<Images/Screenshot (336).png>) 

The output is: 

![Alt text](<Images/Screenshot (320).png>) 

3. Command Substitution: The back tick or the $() syntax is used. 

Example: Using backtick and $() syntax for command substitution. 

![Alt text](<Images/Screenshot (316).png>) 

4. Input and Output: We use read command to accept user input, echo command to output text to the console, and < (input from a file), > (output to a file) and | (pass the output of one command as input to another). 

Example: Accept user input. 

![Alt text](<Images/Screenshot (317).png>) 

Example: Output text to the terminal. 

![Alt text](<Images/Screenshot (322).png>) 

Example: Output the result of a command into a file. 

![Alt text](<Images/Screenshot (318).png>) 

Example: Pass the content of a file as input to a command. 

![Alt text](<Images/Screenshot (319).png>) 

Example: Pass the result of a command as input to another command. 

![Alt text](<Images/Screenshot (321).png>) 

5. Functions: It is used to group related commands together. It modularizes code and make it reuseable. It is defined using the function keyword or the name of the function followed by parentheses. 

Example: Using function. 

![Alt text](<Images/Screenshot (335).png>)

Result: 

![Alt text](<Images/Screenshot (170).png>) 

## Now, We'll Go Into Script Writing Proper By Writing Our First Script. 

Step 1: We'll open a folder on the terminal which will hold all the script we'll write in this project. 

Step 2: We'll create a file that ends with the extension `.sh`. 

Step 3: We'll copy and paste the block of code to use for the script into the new file. 

Step 4: Save the file. 

Step 5: Run `sudo chmod +x user-input.sh` which makes the file executable. 

Step 6: Run the script with `./user-input.sh`

Note: `#!/bin/bash` helps specify the type of bash interpreter to be used to execute the script.

![Alt text](<Images/Screenshot (323).png>) 

![Alt text](<Images/Screenshot (324).png>)

## Directory Manipulation And Navigation. 

The script we're writing will display the current directory, create a new directory called "my_directory", change to that directory, create two files inside it, list the files, move back one level up, remove the "my_directory" and its contents, and finally list the files in the current directory again. 

Step 1: Create a new file. 

Step 2: Paste the code block in the new file. 

![Alt text](<Images/Screenshot (326).png>) 

![Alt text](<Images/Screenshot (340).png>)

Step 3: Run the command `sudo chmod +x navigating-linux-filesystem.sh` to set execute permission on the file.

Step 4: Now, run the script. 

![Alt text](<Images/Screenshot (327).png>) 

## File Operations And Sorting 

This script creates three files, displays the files in their current order, sorts them alphabetically, saves the sorted files in sorted_files.txt, displays the sorted files, removes the original files, renames the sorted file to sorted_files_sorted_alphabetically.txt, and finally displays the contents of the sorted file. 

Step 1: Create a new file. 

![Alt text](<Images/Screenshot (329).png>)

Step 2: Paste the code block into the new file. 

![Alt text](<Images/Screenshot (328).png>)

![Alt text](<Images/Screenshot (338).png>)

Step 3: Set the file's execute permission. 

Step 4: Run the script. 

![Alt text](<Images/Screenshot (330).png>) 

## Working With Numbers And Calculations 

This script defines two variables (num1 and num2) with numeric values, performs basic arithmetic operations(addition, subtraction, multiplication, division, and modulus), and displays the result. It also performs more complex calculations such as raising num1 to the power of 2 and calculating the square root of num2, and displays the results as well. 

Step 1: Create a file using the terminal. 

Step 2: Paste the code block in the file. 

![Alt text](<Images/Screenshot (331).png>) 

Step 3: Set execute permission on the file. 

Step 4: Run the script. 

![Alt text](<Images/Screenshot (332).png>) 

## File Backup And Timestamping 

This script defines the source and backup directory paths. It then creates a timestamp using the current date and time, and creates a backup directory with the timestamp appended to its name.The script then copies all files from the source directory to the backup directory using the `cp` command with `-r` option for recursive copying. Finally, it displays a message indicating the completion of the backup process and shows the path of the backup directory with the timestamp. 

Step 1: Open a new file. 

Step 2: Paste the code block in the new file. 

![Alt text](<Images/Screenshot (342).png>)

Step 3: Set execute permission on the file. 

Step 4: Run the script. 

![Alt text](<Images/Screenshot (341).png>) 

Thank you and God bless you. 