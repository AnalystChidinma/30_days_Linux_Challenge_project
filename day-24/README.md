# Day 24 - Difference Between Bash Script and Shell Script

## Objective

To clearly understand the distinction between Bash scripting and Shell scripting, including their scope, features, compatibility, and real-world usage. This knowledge is essential for writing portable scripts and making informed decisions during system automation and DevOps workflows.

---

## What I Learned

- ### 1. What is a Script?

A script is a sequence of commands stored in a file and executed by an interpreter rather than being compiled.

In Linux, scripts are executed by a shell, which acts as the interface between the user and the operating system kernel.

- ### 2. What is a Shell?

A shell is a command-line interpreter that:

Accepts user commands
Interprets them
Passes them to the kernel for execution

It enables:

Command execution
File manipulation
Process control
Automation via scripting

- ### 3. What is a Shell Script?

A shell script is any script written for a shell interpreter.

Can run on different shells like:
sh (Bourne Shell)
bash
ksh
csh
Used for:
Task automation
System administration
Batch processing

Example: 

#!/bin/sh

myString="Hello Analyst"
echo "myString: $myString"

#### What is Bash Script?

A Bash script is a type of shell script specifically written for the Bash shell.

Bash (Bourne Again Shell) is:

The default shell in most Linux distributions
More powerful and feature-rich than traditional sh

Example:

#!/bin/bash

myString="Hello Analyst"
echo "myString: $myString"

### 5. Key Features of Bash
-  Supports arrays
-  Advanced control structures (if, for, while)
-  Functions
-  Command-line options
-  Better scripting flexibility
-  More developer-friendly syntax

### 6. Key Features of Shell (General)
-  Wildcard expansion (*.txt)
- Piping (|)
-  Background execution (&)
-  Variable substitution
-  Basic scripting support

## Bash Script vs Shell Script (Critical Comparison)

| Feature       | Bash Script                     | Shell Script                          |
|--------------|--------------------------------|---------------------------------------|
| Scope        | Specific to Bash               | General term (any shell)              |
| Compatibility| Limited to Bash                | Can run across different shells       |
| Features     | Advanced (arrays, functions)   | Basic (POSIX standard)                |
| Portability  | Less portable                  | More portable                         |
| Syntax       | Extended syntax                | Minimal syntax                        |
| Shebang      | `#!/bin/bash`                  | `#!/bin/sh`                           |
| Use Case     | Complex scripting              | Simple automation                     |

---

## What I Built / Practiced

- Created both Bash and Shell scripts
- Tested execution differences using:
   - chmod +x script.sh
   - ./script.sh
-  Observed how shebang (#!) determines interpreter behavior

---

## Key Takeaways

- Every Bash script is a shell script, but not every shell script is Bash
- Bash provides advanced scripting capabilities, making it ideal for complex tasks
-  Shell scripting (sh) is preferred when portability across systems is required
-  The shebang line determines which shell executes the script
-  In production environments, choosing the right shell impacts:
      - Compatibility
      - Performance
      - Maintainability

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/bash-script-difference-between-bash-script-and-shell-script/


