# Day 25 - Bash Functions in Linux


## Objective

To understand how to define and use functions in Bash scripting for writing modular, reusable, and efficient scripts. This includes learning how to pass arguments, return values, and manage variable scope within functions.

---

## What I Learned

- ### 1. What are Bash Functions?

A function in Bash is a reusable block of code that performs a specific task.

- Helps reduce repetition (DRY principle)
- Improves readability and maintainability
- Enables modular scripting
- Can accept inputs (arguments) and produce outputs

---

- ### 2. Basic Function Syntax


function_name() {
    commands
}

# Call the function

function_name
- Example:

#!/bin/bash

myFunction() {
    echo "Hello Analyst"
}

myFunction

---
- ### 3. Functions with Arguments

Functions can accept parameters using positional arguments:

$1 → First argument
$2 → Second argument
$n → nth argument

Example:

#!/bin/bash

add_two_num() {
    local sum=$(($1 + $2))
    echo "Sum of $1 and $2 is $sum"
}

add_two_num 2 3

- #### 4. Functions with Return Values

Bash functions return values using the return keyword.

Return values are stored in $?
Only integers between 0–255 are supported

Example:

#!/bin/bash

myfun() {
    return 7
}

myfun
echo "Return value is $?"

Important:

- return is mainly used for status codes, not data transfer
- For real outputs → use echo or command substitution

#### 5. Function with Arguments + Return

#!/bin/bash

add_two_num() {
    return $(($1 + $2))
}

add_two_num 2 3
echo "Sum is $?"

### 6. Variable Scope in Bash Functions

By default:

- All variables are global
- Use local to restrict scope inside functions

Example:

#!/bin/bash

var1="Apple"    global variable

myfun() {
    local var2="Banana"   local variable

    var3="Cherry"         global variable

    echo "First fruit: $var1"

    echo "Second fruit: $var2"
}

myfun

echo "First fruit: $var1"

echo "Second fruit: $var2"

echo "Third fruit: $var3"

#### 7. Overriding Commands

Bash allows redefining built-in commands using functions.

Example:

#!/bin/bash

echo() {
    
    builtin echo "The name is: $1"
}

echo "Chidinma"


---

## Key Takeaways

- Functions are essential for writing clean and scalable scripts
- Always use local variables inside functions to avoid conflicts
- Use echo for returning data, and return for status codes
- Bash functions behave differently from traditional programming languages
- Proper function usage improves script maintainability significantly
---

## Resources

- https://www.geeksforgeeks.org/linux-unix/bash-scripting-functions/

---
