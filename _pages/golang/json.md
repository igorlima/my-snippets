

Pretty Printing JSON Structs in Go

```golang
package main

import (
  "fmt"
  "encoding/json"
)

type Flight struct {
  Origin string `json:"origin"`
  Destination string `json:"destination"`
  Price int `json:"price"`
}

func main() {
  flight := Flight{
    Origin: "GLA",
    Destination: "JFK",
    Price: 2000,
  }

  b, err := json.MarshalIndent(flight, "", "  ")
  if err != nil {
    fmt.Println(err)
  }
  fmt.Print(string(b))
}
```
