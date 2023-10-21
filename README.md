# inMC
in-memory cache

Install:
```
go get github.com/KA-Ryzhkov/inMC
```

Example code:
`````GO
package main

import (
	"fmt"
	inmc "github.com/KA-Ryzhkov/inMC"
)

func main() {
	cache := inmc.New()

	cache.Set("userId", 42)
	cache.Set("user", "Ivan")
	userId := cache.Get("userId")
	user := cache.Get("userName")
	fmt.Println(userId)
	fmt.Println(user)

	cache.Delete("userId")
	cache.Delete("userName")
	userId = cache.Get("userId")
	fmt.Println(userId)
}
