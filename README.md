# swift-tuples
A tutorial wit examples on using tuples in Swift.

# Swift Tuple

In this tutorial, we'll learn about Swift tuples with the help of examples

In Swift, a tuple is a group of different values. 

  - Each value inside a tuple can be of different data types.

Suppose we need to store information about the name and price of a product. 

  - We can create a tuple with a value to store name (`string`) and another value to store price (`float`)

## Create A Tuple

In Swift, we use the parenthesis `()` to store elements of a tuple. For example,

`var product = ("MacBook", 1099.99)`

Here, `product` is a tuple with a string value `Macbook` and integer value `1099.99`.

## Access Tuple Elements

Like an array, each element of a tuple is represented by index numbers (0, 1, ...) where the first element is at index 0.

  - We use the index number to access tuple elements. For example,

```
// access the first element
product.0

// access second element
product.1
Example: Swift Tuple
// create tuple with two elements
var product = ("MacBook", 1099.99)

// access tuple elements
print("Name:", product.0)
print("Price:", product.1)
Output

Name: MacBook
Price: 1099.99
```

In the above example, we have created a tuple named product with two values.

We have used the index number: `product.0` and `product.1` to access tuple elements.

Note: Since the first value of the tuple is a string and the second is an integer, the type of the tuple is (`String, Int`).

## Modify Tuple Element

Modify a tuple element by assigning a new value to the particular index. For example,

```
// create tuple with two elements
var product = ("MacBook", 1099.99)

print("Original Tuple: ")

// access tuple elements 
print("Name:", product.0)
print("Price:", product.1)

// modify second value
product.1 = 1299.99

print("\nTuple After Modification: ")

// access tuple elements
print("Name:", product.0)
print("Price:", product.1)
Output

Original Tuple: 
Name: MacBook
Price: 1099.99

Tuple After Modification: 
Name: MacBook
Price: 1299.99
```

In the above example, we have created a tuple named `product` with values: `MacBook`and `1099.99`. Notice the line,

`product.1 = 1299.99`

Here, we have changed the tuple value at index `1` to `1299.99`.

Note: The tuple index always starts with `0`. The first element of a tuple is present at index `0`, not `1`.

## Named Tuples

In Swift, we can also provide names for each element of the tuple. For example,

`var company = (product: "Programiz App", version: 2.1)`

To access the elements of a named tuple, we can also use these names instead of index numbers.

```
// access "Programiz App"
company.product 
Example: Named Tuple
// create named tuple
var company = (product: "Programiz App", version: 2.1)

// access tuple element using name
print("Product:", company.product)
print("Version:", company.version)
Output

Product: Programiz App
Version: 2.1
```

In the above example, we have provided names: `product` and `version` to the first and the second element of the tuple.


  - We have used the `.` notation and the provided names to access the corresponding values of the tuple.

Note: It is best practice to use the named tuples as it makes our code more readable.

## Swift Nested Tuple

In Swift, we can create a tuple as an element of another tuple. For example,

`var alphabets = ("A", "B", "C", ("a", "b", "c"))`

Here, we have a tuple `("a", "b", "c")` as the third element of the `alphabets` tuple. This is called a nested tuple.

Example: Nested Tuple

```
var alphabets = ("A", "B", "C", ("a", "b", "c"))

// access first element
print(alphabets.0)   // prints "A"

// access the third element
print(alphabets.3)

// access nested tuple
print(alphabets.3.0)  // prints "a"
```
In the above example, notice the line,

`print(alphabets.3)`

Here, we have first accessed the third element of the `alphabets` tuple.

Since the third element is also a tuple, we have used

`alphabets.3.0`

to access the first element of the nested tuple.

## Add/Remove Elements From Tuple

We cannot add or remove elements from a tuple in Swift. For example,

```
var company = ("Programiz","Apple")

company.2 = "Google"

company.remove("Apple")

print(company)
Output

error: cannot convert value of type '(String, String)'
error: value of tuple type '(String, String)' has no member 'remove'
```
Here, we created a tuple with values: "`Programiz`" and "`Apple`". Now, the type of tuple is fixed to (`String, String`).

So, when we try to add and remove elements from the tuple, we get errors.

## Dictionary Inside a Tuple

In Swift, we can use a dictionary to add an element to a tuple. For example,

```
var laptopLaunch = ("MacBook", 1299, ["Nepal": "10 PM", "England": "10 AM"])
print(laptopLaunch.2)

laptopLaunch.2["USA"] = "11 AM"

print(laptopLaunch.2)
Output

["Nepal": "10 PM", "England": "10 AM"]
["Nepal": "10 PM", "England": "10 AM", "USA": "11 AM"]
```

In the above example, the third element of the tuple is a dictionary

`["Nepal": "10 PM", "England": "10 AM"]`

As we know we can add elements to a dictionary. So, we use the code.

`laptopLaunch.2["USA"] = "11 AM"`

to add an element inside the dictionary.

This way we are able to add an element to a tuple. And, the type of tuple is still the same (String, String, Dictionary). So, we don't get any errors.
