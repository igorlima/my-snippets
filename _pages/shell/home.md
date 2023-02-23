---
title: Shell
author: Igor Lima
date: 2023-02-23
category: shell
layout: post
---

## Bash scripting syntax

setting variables
```sh
TEST_VAR='Hello World!'
export TEST_VAR='Hello World!'
```

accessing variable
```sh
echo $TEST_VAR
# if the variable is not specified, we can use the default value.
echo ${TEST_VAR:-hello world}
```

test command
```sh
# there are two syntaxes for using the test command
test EXPRESSION
[ EXPRESSION ]

# = and == are for string comparisons
# -eq is in the same family as -lt, -le, -gt, -ge, and -ne
if [ 1 -eq 1 ]; then echo 1; else echo 0; fi
if [ 1 -eq 0 ]; then echo 1; else echo 0; fi
if test 1 -eq 1; then echo 1; else echo 0; fi
if test 1 -eq 0; then echo 1; else echo 0; fi
```

exclamation mark
```sh
# exclamation mark in bash is often used to reverse the logic of the expression. if the expression is true, the ! operator will return false. and vice versa.
var="hello"
if [ ! "$var" = "hello" ]; then
  echo "var is not hello"
else
  echo "var is hello"
fi
```

bash variable $?
```sh
# '$?' is used to find the return value of the last executed command.
# if the last command was successful, then $? will be 0. if the previous command was unsuccessful, then $? will be non-zero.
ls xxx
if [ $? -eq 0 ]; then
  echo "The last command was successful."
else
  echo "The last command was unsuccessful."
fi
```

## test A

### test B

#### test C
