# Bash Scripts

## **Intro:**

Shell scripting is an important part of process automation in Linux. 

A bash script is a series of commands written in a file. These are read and executed by the bash program. Bash executes line by line.

e.g you can navigate to a certain path, create a folder and spawn a process inside it using the command line OR ALTERNATIVELY you can do the same sequence of steps by saving the commands in a bash script and running it 

**Bash:** A command-line tool to interact with your computer.

**Bash Script:** A file containing a series of commands you want the computer to execute automatically.

Bash scripting helps to:
1. **Automate tasks:** Save time on repetitive actions.
2. **Manage systems:** Handle files, software installs, and system configurations.
3. **Boost efficiency:** Get more done with less typing!

## The logistics 

**Identification:**

Bash scripts have a file extension of **.sh** 

**Shebang (#!):**
- The first line of script is #!/bin/bash (its simply an absolute path to the bash interpreter and therefore tells the computer to use Bash to run the script)

Since this just serves as a directive to the OS on how to interpret the script, there's variations:
- #!/bin/bash
- #!/bin/ruby
- #!/bin/python
  
**Execution rights:**

Scripts have execution rights for the user executing them so you need to make the file executable using chmod +x your_script.sh 

The scripts with execution rights appear as green (changes colour)

**Run Your Script:**

1. ./nameoffile.sh
2. sh nameoffile
3. bash nameoffile
4. You can add your script to one of the directories in the PATH environment variable, you can run the script from anywhere in the terminal. 

## **How to create a simple bash script**

1. Create file: touch my-first-script.sh
2. Write the command: vim my-first-script.sh

#! /usr/bin/bash
echo "Hello World"

3. Provide execution rights to your user: chmod +x my-first-script.sh 
4. Run the scrip: ./my-first-script.sh 

Hello World!

## **Basic Syntax of Bash Scripting**

**Comments:**
This is best practice to clearly udnerstand the purpose, functionality and logic of the script.

- single line comment e.g #
- multi-line comment e.g : ' many diff lines of comments '

**Variables:**
Allow you to store and manipulate data such as strings, numbers, arrays. They are created using the assingment operator '=' and use $ to access said variable

Variables can hold different types of data including:
- strings - sequences of characters enclosed in either (') or (")
- numbers - count=42
- arrays - hold multiple values and uses () e.g fruits=("apple" "banana" "cherry")

**How they work:**

- **Store values:** greeting="hello world" (This assigns the string "hello world" to a variable named greeting.It doesn't produce any output on its own; it just stores the value "hello world" in memory which is why the following line is teh echo commmand to produce the output)
- **Use them:** echo $greeting

**Variable interpolation** 
allows you to use varaibles within strings to create synamic output

- **Store values:** name="Ahmed"
- **Use them:** echo "Hello, $name"

This takes the name variable and assigns it within the string so the input is Hello, Ahmed

## Parameters

Parameters (aka arguments) allow you to provide input values to a script or function which customsies its behaviour based on those inputs

You place parameters after the script name - ./script.sh Parameter1 Parameter2

Inside the script, you access each parameter using $1, $2, $3 etc 

Example:
- echo "Parameter 1: $1"
- echo "Parameter 2: $2"
- echo "Parameter 3: $3"

- echo "All Parameters: $@" - $@: displays all arguments as a list

## Arithmetic expansion 

Allows you to calculate things using values of variables and parameters and displays result using echo command

This:
Makes scripts dynamic and flexible (due to use of var&para)
Gives a precise and readble syntax $(())

Use of variables:
here you explicitly assign values to variables

- length=10
- width=20

Use of parameters:
here positional parameters are passed to the script (more flexible)

- length="$1"
- width="$1"

## If statements (conditional statements)

Used to test conditions and execute different commands based on the outcome of those conditions (true or false)

**Key Components:**

- **if:** Starts the conditional check.
- **[ condition ]:** The condition to evaluate. Returns true (0) or false (non-zero).
- **then:** If the condition is true, execute the following commands.
-     **INSERT CODE BLOCK**
- elif (optional): Allows additional conditions to check if the first one is false.
- else (optional): Specifies what to do if all conditions are false.
- **fi:** Ends the if statement block.

| Operator | Description              | Example                  |
|----------|--------------------------|--------------------------|
| `-eq`    | Equal to                 | `[ "$1" -eq "$2" ]`      |
| `-ne`    | Not equal to             | `[ "$1" -ne "$2" ]`      |
| `-lt`    | Less than                | `[ "$1" -lt "$2" ]`      |
| `-le`    | Less than or equal to    | `[ "$1" -le "$2" ]`      |
| `-gt`    | Greater than             | `[ "$1" -gt "$2" ]`      |
| `-ge`    | Greater than or equal to | `[ "$1" -ge "$2" ]`      |




