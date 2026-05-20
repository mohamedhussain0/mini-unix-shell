# mini-unix-shell 🐚

A minimal Unix shell built in C, supporting built-in commands: `pwd`, `echo`, `history`, `env`, `cd`, and `exit`.

---

## 📋 Table of Contents

- [About](#about)
- [Built-in Commands](#built-in-commands)
- [Getting Started](#getting-started)
- [Usage Examples](#usage-examples)
- [Project Structure](#project-structure)

---

## About

This project is a minimal Unix shell implemented from scratch in C.  
It supports a set of built-in commands handled directly by the shell, as well as the ability to launch any external program using `fork()` + `execvp()`.

Based on the original [LSH](https://brennan.io/2015/01/16/write-a-shell-in-c/) by Stephen Brennan, extended with additional built-in commands.

---

## Built-in Commands

| Command | System Call | Description |
|---|---|---|
| `pwd` | `getcwd()` | Print the current working directory |
| `echo [args]` | `printf()` | Print arguments separated by spaces |
| `history` | Internal array | Print previously entered commands, numbered |
| `env` | `extern char **environ` | Print all environment variables in `KEY=VALUE` format |
| `cd [dir]` | `chdir()` | Change the current working directory |
| `help` | — | List all available built-in commands |
| `exit` | — | Exit the shell |

---

## Getting Started

### Requirements

- GCC
- Linux / macOS (any Unix-like system)

### Build

```bash
gcc -Wall -o lsh main.c
```

### Run

```bash
./lsh
```

---

## Usage Examples

```bash
> pwd
/home/user/mini-unix-shell

> echo Hello World
Hello World

> cd /tmp
> pwd
/tmp

> history
  1  pwd
  2  echo Hello World
  3  cd /tmp
  4  pwd
  5  history

> env
HOME=/home/user
PATH=/usr/local/bin:/usr/bin:/bin
PWD=/tmp
...

> exit
```

---

## Project Structure

```
mini-unix-shell/
├── main.c       # Full shell implementation
└── README.md
```
