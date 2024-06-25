## Data Structures in Original Language

### Introduction

Original Language supports a variety of data structures to store and manipulate data efficiently. This section introduces the built-in data structures and how to use them effectively in your programs.

#### Supported Data Structures

- **Lists**: Dynamic arrays capable of holding elements of different types.
- **Dictionaries**: Key-value pairs for efficient lookup and storage.
- **Sets**: Collections of unique elements, useful for mathematical operations.
- **Records**: Custom data structures with named fields, allowing structured data organization.

### Lists

#### Syntax

Lists in Original Language are defined using square brackets `[]` and can contain elements of any type.

##### Example

```plaintext
let numbers = [1, 2, 3, 4, 5];
let fruits = ["apple", "banana", "orange"];
```

#### Operations

- **Accessing Elements**: Use index notation `[index]` to access elements.
- **Appending Elements**: Use `push` method to add elements to the end.
- **Iterating**: Use `for element in list { ... }` to iterate over elements.

##### Example

```plaintext
let numbers = [1, 2, 3];
print(numbers[0]);  # Output: 1

numbers.push(4);
for num in numbers {
    print(num);
}
```

### Dictionaries

#### Syntax

Dictionaries in Original Language use curly braces `{}` and store key-value pairs where keys and values can be of any type.

##### Example

```plaintext
let ages = {"Alice": 30, "Bob": 25, "Carol": 28};
```

#### Operations

- **Accessing Values**: Use `dict[key]` to retrieve values by key.
- **Adding/Updating Entries**: Assign a value to a key to add or update entries.
- **Iterating**: Use `for key in dict { ... }` to iterate over keys or `for key, value in dict { ... }` to iterate over key-value pairs.

##### Example

```plaintext
let ages = {"Alice": 30, "Bob": 25, "Carol": 28};
print(ages["Alice"]);  # Output: 30

ages["David"] = 22;  # Adding a new entry
for person in ages {
    print(person + " is " + ages[person] + " years old");
}
```

### Sets

#### Syntax

Sets in Original Language are defined using curly braces `{}` and store unique elements.

##### Example

```plaintext
let unique_numbers = {1, 2, 3, 4, 5};
```

#### Operations

- **Adding Elements**: Use `add` method to add elements to the set.
- **Set Operations**: Supports operations like union, intersection, and difference.
- **Iterating**: Use `for element in set { ... }` to iterate over elements.

##### Example

```plaintext
let set1 = {1, 2, 3};
let set2 = {3, 4, 5};

let union_set = set1.union(set2);
print(union_set);  # Output: {1, 2, 3, 4, 5}
```

### Records

#### Syntax

Records in Original Language are defined using the `record` keyword and consist of named fields with specified types.

##### Example

```plaintext
record Person {
    name: string;
    age: int;
}
```

#### Operations

- **Creating Instances**: Instantiate records with specified values for each field.
- **Accessing Fields**: Use dot notation (`record.field`) to access fields.

##### Example

```plaintext
let person = Person{name: "Alice", age: 30};
print("Name: " + person.name + ", Age: " + person.age);
```

## Control Flow in Original Language

### For Loops

For loops in Original Language allow iterating over collections such as lists, sets, and dictionaries.

#### Syntax

```plaintext
let numbers = [1, 2, 3, 4, 5];
for num in numbers {
    print(num);
}
```

#### Operations

- **Iterating**: Use `for item in collection { ... }` to iterate over elements in a collection.
- **Support for Lists, Sets, and Dictionaries**: Iterate over elements in lists, sets, or key-value pairs in dictionaries.

##### Example

```plaintext
let fruits = ["apple", "banana", "orange"];
for fruit in fruits {
    print("Fruit: " + fruit);
}

let ages = {"Alice": 30, "Bob": 25, "Carol": 28};
for person, age in ages {
    print(person + " is " + age + " years old");
}
```
