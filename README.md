### Install
```
go get -u github.com/gofiber/fiber
go get -u github.com/gofiber/cors
```
### Example
```go
package main

import (
  "github.com/gofiber/fiber"
  "github.com/gofiber/cors"
)

func main() {
  app := fiber.New()

  app.Use(cors.New())

  app.Get("/", func(c *fiber.Ctx) {
    c.Send("Welcome!")
  })

  app.Listen(3000)
}
```
### Test
```curl
curl -H "Origin: http://example.com" --verbose http://localhost:3000
```
