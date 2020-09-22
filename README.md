# Closures

A closure is either one of the following.
- Global Function
- Nested Function
- Closure Expression/ Unnamed

## Functions

Every function in Swift has a type, which will consist of the function's parameter types and its return type.

The simplest type a function can have for its parameters or return type is `()` or `Void`.

Valid
```swift
() -> ()
() -> Void
() -> (Void)
```

Invalid
```swift
// When calling this function in Swift 4 or later, you must pass a '()' tuple; did you mean for the input type to be '()'?
(Void) -> ()

// Single argument function types require parentheses
Void -> ()
```

### Understanding Function Types

#### Function with 0 parameters and returns Void
```swift
// () -> ()
func basic() {
	print("Hello, World!")
}

basic() // output: "Hello, World!"

let basicFunction: () -> () = basic

basicFunction() // output: "Hello, World!"
```

#### Function with 1 parameter and returns Void
```swift
// (String) -> ()
func basic(withValue value: String) {
	print("Hello, World! (withValue: \(value))")
}

basic(withValue: "some value") // output: "Hello, World! (withValue: some value)"

let basicFunction: (String) -> () = basic

basicFunction("some value") // output: "Hello, World! (withValue: some value)"
```

#### Function with 1 parameter and returns a String
```swift
// (String) -> String
func basic(withValue value: String) -> String {
	"Hello, World! (withValue: \(value))"
}

print(basic(withValue: "String")) // output: "Hello, World! (withValue: String)"

let basicFunction: (String) -> String = basic

print(basicFunction("String")) // output: "Hello, World! (withValue: String)"
```

