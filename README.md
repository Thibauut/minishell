# Minishell - Linux Shell Interpreter

A minimalist Linux shell interpreter that replicates the core functionalities of a Unix/Linux shell. This project is designed to execute basic commands, handle input/output redirection, and manage processes effectively. It demonstrates key concepts of system programming and the use of POSIX APIs.

## Features

- **Command Execution**: Supports built-in Linux commands (e.g., `ls`, `cd`, `mkdir`, etc.).
- **Input/Output Redirection**:
  - Redirect standard input (`<`), output (`>`), and append (`>>`).
- **Pipes**:
  - Allows command chaining using `|` (e.g., `ls | grep filename`).
- **Process Management**:
  - Executes commands in both foreground and background modes (`&`).
- **Signal Handling**:
  - Graceful handling of `Ctrl+C` and other common signals.
- **Error Handling**:
  - Provides meaningful error messages for invalid commands or missing arguments.

## Usage

1. Clone the repository:

   ```bash
   git clone git@github.com:Thibauut/minishell.git
   ```

2. Compile the project:

   ```bash
   make re
   ```

3. Run the shell:

   ```bash
   ./minishell
   ```

4. Start typing commands just like you would in a standard Linux terminal. For example:

   ```bash
   ls -la
   grep "pattern" file.txt
   echo "Hello, World!" > output.txt
   cat output.txt
   ./your_program
   ```

## Examples

### Example 1: Basic Command Execution

```bash
$ ls -l
-rw-r--r-- 1 user user  4096 Dec 15 12:00 file.txt
```

### Example 2: I/O Redirection

```bash
$ echo "Hello, Shell!" > output.txt
$ cat < output.txt
Hello, Shell!
```

### Example 3: Piping

```bash
$ ls | grep "file"
file.txt
```

### Example 4: Background Process

```bash
$ ./long_running_task &
[1] 12345
```

## Requirements

- **Operating System**: Linux or Unix-based OS
- **Compiler**: GCC or G++
- **Development Tools**: Makefile (optional but recommended)

## Learning Objectives

This project helped me gain a deeper understanding of:

- POSIX system calls and process management.
- Command parsing and handling shell-specific syntax.
- File descriptors and I/O redirection in Unix.
- Implementing piping and inter-process communication.
- Signal handling and graceful termination of processes.

