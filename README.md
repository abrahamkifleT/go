# Go (Golang) - From Basics to REST API

## 1. Introduction to Go

- **Why Go?**: Simple, efficient, great for backend systems.
- **Setting Up**: Install Go [here](https://golang.org/dl/).
- **First Program**: Run `hello.go`

  ```go
  package main

  import "fmt"

  func main() {
      fmt.Println("Hello, Go!")
  }
  ```

## 2. Basics of Go

- **Data Types**: int, string, bool, float64
- **Variables**: `var`, `:=` shorthand
- **Functions**: `func` keyword, parameters, and return types

  ```go
  func add(a int, b int) int {
      return a + b
  }
  ```

## 3. Working with Packages

- Use `import` to add libraries
- Standard library overview: `fmt`, `net/http`, `os`

## 4. Building a REST API

1. **Set Up HTTP Server**

   ```go
   package main

   import (
       "fmt"
       "net/http"
   )

   func helloHandler(w http.ResponseWriter, r *http.Request) {
       fmt.Fprintf(w, "Hello, REST API!")
   }

   func main() {
       http.HandleFunc("/", helloHandler)
       http.ListenAndServe(":8080", nil)
   }
   ```

2. **Creating CRUD Endpoints**

   - **GET**: Retrieve data
   - **POST**: Create data
   - **PUT**: Update data
   - **DELETE**: Remove data

3. **Testing**: Use tools like Postman or `curl` to test endpoints.
