# LSH: A Simple Shell

This project is a simple command-line shell (LSH) written in C. It supports a few built-in commands and can execute external programs.

## Features

- Built-in commands: `cd`, `help`, and `exit`.
- Ability to execute external programs.
- Uses system calls to create new processes (`fork()`) and execute programs (`execvp()`).

## Usage

To compile and run the program, enter the following commands in the terminal:

```sh
gcc -o lsh main.c
./lsh
```

After running the program, you can enter your commands. For example:

```sh
> help
> cd ..
> ls -l
> exit
```

## Built-in Commands

1. **cd**: Change the directory.
   - Usage: `cd <directory_name>`
   - Example: `cd /home/user`

2. **help**: Display this help message.
   - Usage: `help`

3. **exit**: Exit the shell.
   - Usage: `exit`

## Code Structure

- `main.c`: The main file that contains all the necessary functions to run the shell.
- `builtin_func[]` and `builtin_str[]`: Arrays that store the built-in commands and their corresponding functions.
- Built-in command functions:
  - `lsh_cd(char **args)`: Changes the current directory.
  - `lsh_help(char **args)`: Displays help information.
  - `lsh_exit(char **args)`: Exits the shell.

## Author

This project was created by Lord_Smh.
