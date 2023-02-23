---
title: Golang Pointer
author: Igor Lima
date: 2023-02-23
category: Golang
layout: post
---

a one-pager to understanding pointers in Go

```golang
package main

import "fmt"

func main() {
  // a pointer is a variable that holds the memory address of another variable
  var p1 *int
  x := 42
  y := 40
  // to create a pointer to a variable, use the & operator followed by the variable's name
  p1 = &x
  p2 := &y
  // to access the value of the variable pointed to by a pointer, you use the * operator followed by the pointer variable name
  *p1 = 100

  increment(&y)
  increment(p2)

  fmt.Println(x)
  fmt.Println(p2)
  fmt.Println(&p2)
  fmt.Println(*p2)
}

// passing pointers to functions
// one common use of pointers is to pass a variable to a function by reference, allowing the function to modify the variable directly.
func increment(p *int) {
  *p++
}
```
