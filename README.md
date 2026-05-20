# mini-unix-shell
A minimal Unix shell built in C, supporting built-in commands: pwd, echo, history, env, cd, and exit.
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
