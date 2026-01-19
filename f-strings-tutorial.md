# Using f-Strings to Build Strings in Python

When you write Python programs, you often need to combine text with values stored in variables. For example, you might want to create a personalized greeting for a user or display someone's score in a game. Python offers several ways to handle this task, but **f-strings** are the modern and preferred approach.

In this tutorial, you'll learn how to use f-strings to interpolate values into your strings.

**By the end of this tutorial, you'll understand that:**

* An **f-string** is a string literal prefixed with `f` that lets you embed expressions inside curly braces
* You can **interpolate** variables, numbers, and calculations directly into strings using f-strings
* F-strings make your code more **readable** and **concise** compared to older formatting methods

## Why Python Has f-Strings

Before Python 3.6 introduced f-strings, formatting strings often involved extra steps. You might have used the modulo operator (`%`) or the `.format()` method. These approaches worked, but they made code harder to read and more prone to errors.

F-strings solve these problems by letting you describe the final output directly. Instead of building strings piece by piece, you write the result you want to see, with variables embedded right where they belong.

## Creating Your First f-String

To create an f-string, you prefix a string literal with the letter `f`. Inside the string, you place variables inside curly braces `{}`:

```python
name = "John Doe"

print(f"Hello, {name}!")
```

When you run this code, you'll get the following output:

```
Hello, John Doe!
```

Python replaces `{name}` with the actual value `"John Doe"` when building the final string.

## Using Numbers Inside f-Strings

F-strings aren't limited to text. You can include integers and other data types directly:

```python
age = 21

print(f"You are {age} years old.")
```

This produces:

```
You are 21 years old.
```

Python automatically converts the integer to a string when building the output. You don't need to manually convert types.

## Embedding Expressions in f-Strings

You can embed expressions, not just variable names. This means you can perform calculations directly inside your string:

```python
price = 50
quantity = 3

print(f"Total cost: ${price * quantity}")
```

This produces:

```
Total cost: $150
```

Python evaluates `price * quantity` before inserting the result. This keeps related logic and output close together.

You can also call methods inside f-strings:

```python
name = "jane"

print(f"Hello, {name.upper()}!")
```

This gives you:

```
Hello, JANE!
```

The f-string calls the `.upper()` method on `name` and inserts the uppercased result.

## When to Use f-Strings

You should reach for f-strings whenever you need to combine text with variables or calculations. They're particularly useful for user messages, log entries, or any output where readability matters.

For example, `f"Welcome back, {username}!"` is clearer than `"Welcome back, " + username + "!"` or `"Welcome back, {}!".format(username)`.

F-strings help you write code that communicates its intent clearly to both Python and anyone reading your code.
