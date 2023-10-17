# inMC
in-memory cache

Example code:


`````GO
import (
    "fmt"
    "github.com/KA-Ryzhkov/inMC"
)

func main() {
    cache := New()

	cache.Set("userId", 42)
	cache.Set("user", "Ivan")
	userId := cache.Get("userId")
	user := cache.Get("user")
	fmt.Println(userId)
	fmt.Println(user)

	cache.Delete("userId")
	cache.Delete("user")
	userId = cache.Get("userId")
	fmt.Println(userId)
}
