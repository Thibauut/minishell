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

## Project Structure

```
minishell/
├── Makefile
├── README.md
├── include
│   └── my.h
├── minishell.c
└── src
    ├── builtin
    │   ├── my_cd.c
    │   ├── my_cd2.c
    │   ├── my_env.c
    │   ├── my_exit.c
    │   ├── my_setenv.c
    │   ├── my_setenv2.c
    │   └── my_unsetenv.c
    ├── my_check_cmd.c
    ├── my_error.c
    ├── my_exec.c
    ├── my_func.c
    ├── my_func2.c
    ├── my_func3.c
    ├── my_get_arg.c
    ├── my_get_arg2.c
    ├── my_get_arg_double.c
    ├── my_get_path.c
    ├── my_minishell.c
    ├── my_tab_and_space.c
    └── symbol
        ├── my_entry.c
        ├── my_pipe.c
        ├── my_pipe2.c
        ├── my_redirection.c
        └── my_semicolon.c
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

