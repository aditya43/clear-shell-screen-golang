# About
Cross platform (Linux, OS X and Windows) clear shell screen written in Go lang.

## Author
Aditya Hajare ([Linkedin](https://in.linkedin.com/in/aditya-hajare)).

## Installation
```
$ go get -u github.com/aditya43/clear-shell-screen-golang
```

## How To Use?
```go
package main

import (
	"fmt"
	"time"

	"github.com/aditya43/clear-shell-screen-golang"
)

func main() {
	// Clear all the characters on the screen
	screen.Clear()

	for {
		// Moves the cursor to the top-left position of the screen
		screen.MoveTopLeft()

		// Animate the time always in the same position
		fmt.Println(time.Now())

		time.Sleep(time.Second)
	}
}
```

## Width and Height
To get the current terminal width and height.
```go
package main

import (
	"fmt"
	"github.com/aditya43/clear-shell-screen-golang"
)

func main() {
	w, h := screen.Size()

	fmt.Printf("Width: %d Height: %d\n", w, h)
}
```