Lists and dictionaries can be combined in powerful ways. For example, you could store lists as dictionary values, or nest dictionaries inside other dictionaries. This creates flexible data structures for organizing complex information in a hierarchy.

# Lists as Dictionary Values

Since dictionary values can be any type, you can store lists as values:

```py-cell
student = {"name": "Alice", "grades": [90, 85, 92]}
print(student)

student["subjects"] = ["Math", "English", "Science"]
print(student)
```

Each value is a list, so you can access individual items using additional indexing:

```py-cell
student = {"name": "Alice", "grades": [90, 85, 92]}

print(student["grades"])      # Get the list of grades
print(student["grades"][0])   # Get first grade
print(student["grades"][-1])  # Get last grade
```

You can also modify the list values using list methods:

```py-cell
student = {"name": "Alice", "grades": [90, 85]}

student["grades"].append(92)
print(student)
```

# Nested Dictionaries

Dictionaries can also contain other dictionaries as values, creating nested structures:

```py-cell
person = {"name": "Alice"}
person["address"] = {"city": "London", "postcode": "SW7 2AZ"}

print(person)

print(person["address"]["city"])
```

To access a value in a nested dictionary, use chained bracket notation: `person["address"]["city"]`{.python}. This tells Python to get the `address`{.python} value from `person`{.python}, then get the `city`{.python} value from that dictionary.
