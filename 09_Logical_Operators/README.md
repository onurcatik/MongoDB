# MongoDB Logical Operators Tutorial

Logical operators in MongoDB are powerful tools for querying data based on expressions that evaluate to true or false. In this tutorial, we'll explore the four main logical operators: $and, $or, $nor, and $not, with detailed explanations and code snippets.

### 1. Using $and Operator

The $and operator returns documents where all specified conditions are true.

**Example:**

```javascript
db.students.find({
  $and: [
    { full_time: true }, // Condition 1: Full-time student
    { age: { $lte: 22 } } // Condition 2: Age less than or equal to 22
  ]
})
```

This query will return students who are both full-time and 22 years or younger.

### 2. Using $or Operator

The $or operator returns documents where at least one of the specified conditions is true.

**Example:**

```javascript
db.students.find({
  $or: [
    { full_time: true }, // Condition 1: Full-time student
    { age: { $lte: 22 } } // Condition 2: Age less than or equal to 22
  ]
})
```

This query will return students who are either full-time or 22 years or younger.

### 3. Using $nor Operator

The $nor operator returns documents where none of the specified conditions are true.

**Example:**

```javascript
db.students.find({
  $nor: [
    { age: { $gt: 22 } }, // Condition 1: Age greater than 22
    { full_time: true } // Condition 2: Full-time student
  ]
})
```

This query will return students who are neither older than 22 nor full-time.

### 4. Using $not Operator

The $not operator performs a logical NOT operation on the specified condition(s).

**Example:**

```javascript
db.students.find({
  $not: { age: { $gte: 30 } } // Condition: Age not greater than or equal to 30
})
```

This query will return students whose age is not greater than or equal to 30.

### Handling Null Values with $not Operator

The $not operator can also handle null values effectively.

**Example:**

```javascript
db.students.find({
  $not: { age: { $gte: 30 } } // Condition: Age not greater than or equal to 30 (including null values)
})
```

This query will return students whose age is not greater than or equal to 30, including those with null values.
