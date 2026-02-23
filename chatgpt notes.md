Perfect 👍
Below is **your exact content**, cleaned and converted into proper `.md (Markdown)` format.
You can copy this directly and save as:

```
shell-scripting-notes.md
```

---

# Shell Scripting

#shell scripting123

---

# What is Shell?

* Shell refers to a user interface that allows users to interact with the operating system (OS) or execute commands.
* It acts as a command interpreter, taking commands entered by the user (via a command-line interface or graphical interface) and executing them by communicating with the OS kernel.
* In most Linux OS, **BASH (Bourne Again Shell)** is the default shell type.

There are other shell programs:

1. Korn Shell (ksh)
2. Bash
3. C Shell (csh)
4. Z Shell (zsh)

---

## How to check how many shells are there in my Linux server?

```
cat /etc/shells
```

---

## How to install csh / zsh / ksh?

```
sudo yum install csh -y
sudo yum install zsh -y
sudo yum install ksh -y
```

---

## How to check which shell we are using now?

```
echo $SHELL
echo $0
ps -p $$
```

---

## How to switch to another shell?

**Step 1:** Check available shells

```
cat /etc/shells
```

**Step 2:** Switch shell

```
/bin/sh
ps -p $$
```

**Step 3:** Come back to bash

```
/bin/bash
```

---

# What is Shell Scripting?

* It is a file that contains a collection of commands.
* Whatever order we specify, based on that order it will be executed.

---

## What is the extension for shell scripting?

```
.sh
```

---

## Why do we need to learn shell scripting?

To automate manual tasks.

Examples:

* serverresourseutilization.sh
* dbbackup.sh

---

## Is it only for DevOps Engineers?

NO

---

## Prerequisites to learn shell scripting

1. Linux commands
2. Basic programming knowledge (optional but helpful)
3. Commitment
4. Problem-solving skills

---

# How to write a shell script?

```
vi Demo.sh
```

Add:

```
#!/bin/bash
echo "Welcome to shellscript KK FUNDA"
echo "Today date is"
date
```

---

## Shebang Line

```
#!/bin/bash
```

---

# How many ways to run a script?

1.

```
sh Demo.sh
```

2.

```
chmod u+x Demo.sh
./Demo.sh
```

3.

```
. Demo.sh
```

4.

```
bash Demo.sh
```

---

# How to run script in debug mode?

1.

```
sh -x Demo.sh
```

2. Debug only specific part:

```
set -x
echo "Welcome to shellscript KK FUNDA"
echo "Today date is"
set +x
date
```

---

# Comments in Shell Scripting

* Improve readability
* Document script
* Explain commands

### Single-line comment

```
# This is a single-line comment
```

### Inline comment

```
command1  # This command does something
```

### Multi-line comment (manual way)

```
# Line 1
# Line 2
# Line 3
```

---

# Variables in Shell Scripting

## Definition

Variables are used to store data or values that can be referenced and manipulated throughout the script.

---

## Variable Naming Rules

* Letters (a-z, A-Z), digits (0-9), underscore (_)
* Must start with letter or underscore
* Case-sensitive

---

## Variable Assignment

```
myVar="Hello, World!"
```

No spaces around `=`.

---

## Accessing Variables

```
echo "The value of myVar is: $myVar"
```

---

## Types of Variables

### Environment Variables (System-defined)

```
env
printenv
echo $USER
```

Temporary change:

```
export HISTSIZE=300
```

Permanent change:

Edit:

```
~/.bash_profile
```

---

### Local (User-defined) Variables

```
a=10
b=90
name="kkfunda"

echo $a
echo $b
echo $name
```

---

# Command Line Arguments

```
$0  -> Script name
$1  -> First argument
$2  -> Second argument
${10} -> Tenth argument
```

Example:

```
echo "Script name: $0"
echo "First argument: $1"
echo "Second argument: $2"
```

---

## Special Variables

```
$#   -> Number of arguments
$@   -> All arguments (separate)
$*   -> All arguments (single string)
$$   -> Process ID
$?   -> Previous command status
```

Exit codes:

```
0   -> Success
127 -> Command not found
```

---

# Read Command

Basic input:

```
read name
```

With prompt:

```
read -p "Enter your age: " age
```

Silent input:

```
read -s -p "Enter your password: " password
```

Timeout:

```
read -t 10 name
```

---

# Operators in Shell Scripting

## Arithmetic

```
$(( a + b ))
$(( a - b ))
$(( a * b ))
$(( a / b ))
$(( a % b ))
```

---

## Comparison

```
-eq
-ne
-gt
-lt
-ge
-le
```

---

## Logical

```
&&   (AND)
||   (OR)
!    (NOT)
```

---

## String Operators

```
= 
!=
${#str}  (length)
```

---

# Control Statements

## If

```
if [ condition ]
then
   commands
fi
```

---

## If-Else

```
if [ condition ]
then
   commands
else
   commands
fi
```

---

## If-Elif-Else

```
if [ condition ]
then
   commands
elif [ condition ]
then
   commands
else
   commands
fi
```

---

## Case Statement

```
case $var in
   pattern1)
      commands
      ;;
   *)
      default
      ;;
esac
```

---

# Loops

## For Loop

```
for i in 1 2 3 4 5
do
   echo $i
done
```

C-style:

```
for (( i=1; i<=5; i++ ))
do
   echo $i
done
```

---

## While Loop

```
while [ condition ]
do
   commands
done
```

---

## Until Loop

```
until [ condition ]
do
   commands
done
```

---

# Arrays

Declare:

```
arr=("kk" "sai" "raghu")
```

Access:

```
echo ${arr[0]}
```

Length:

```
echo ${#arr[@]}
```

Loop:

```
for i in "${arr[@]}"
do
   echo $i
done
```

---

# Functions

Define:

```
function_name() {
   commands
}
```

Example:

```
greet() {
   echo "Hello"
}
greet
```

---

## Function with Parameters

```
sum() {
   local a=$1
   local b=$2
   echo $((a+b))
}
sum 10 20
```

---

# File Descriptors

```
0 -> stdin
1 -> stdout
2 -> stderr
```

Redirection:

```
>      overwrite
>>     append
<      input
2>&1   redirect error to output
```

---

# Cron Job Example

```
0 2 * * * /path/to/delete.sh
```

Runs daily at 2:00 AM.

---

If you want next:

* Full advanced version (with all your real-time examples added)
* Interview questions from this data
* Practice exercises
* Mini projects

Tell me 👍
