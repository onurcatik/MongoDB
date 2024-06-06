# Data Types

MongoDB is a popular NoSQL database that offers flexibility in data modeling, allowing you to store various data types within documents. In this tutorial, we will explore the basic data types supported by MongoDB and how to use them effectively.

## 1. String

A string is a series of text characters enclosed within quotes. It can be single quotes (`'`) or double quotes (`"`). Let's insert a document into our MongoDB collection `students` with a string field `name`.

```javascript
db.students.insertOne({
    name: "Larry Lobster"
});
```

In this example, `"Larry Lobster"` is a string value representing the name of the student.

## 2. Integer

An integer is a whole number without a decimal portion. Let's add an `age` field for our student Larry.

```javascript
{
    name: "Larry Lobster",
    age: 32
}
```

Here, `32` is an integer representing Larry's age.

## 3. Double

A double is a number that contains a decimal portion. It's suitable for storing values like GPA (Grade Point Average). Let's include a `gpa` field for Larry.

```javascript
{
    name: "Larry Lobster",
    age: 32,
    gpa: 2.8
}
```

In this case, `2.8` is a double representing Larry's GPA.

## 4. Boolean

A boolean data type can have only two values: `true` or `false`. It's useful for representing binary states like "full-time" or "part-time" status. Let's add a `full_time` field for Larry.

```javascript
{
    name: "Larry Lobster",
    age: 32,
    gpa: 2.8,
    full_time: false
}
```

Here, `false` indicates that Larry is a part-time student.

## 5. Date

Date objects represent points in time. MongoDB uses the `Date` data type for storing dates. Let's add a `registration_date` field for Larry.

```javascript
{
    name: "Larry Lobster",
    age: 32,
    gpa: 2.8,
    full_time: false,
    registration_date: new Date()
}
```

This will set `registration_date` to the current date and time.

## 6. Null

The null data type represents the absence of a value. It can be useful as a placeholder. Let's add a `graduation_date` field for Larry.

```javascript
{
    name: "Larry Lobster",
    age: 32,
    gpa: 2.8,
    full_time: false,
    registration_date: new Date(),
    graduation_date: null
}
```

Here, `graduation_date` is set to `null` as we don't have that information yet.

## 7. Arrays

Arrays allow storing multiple values within a single field. Let's add a `courses` field for Larry to store the courses he's enrolled in.

```javascript
{
    name: "Larry Lobster",
    age: 32,
    gpa: 2.8,
    full_time: false,
    registration_date: new Date(),
    graduation_date: null,
    courses: ["biology", "chemistry", "calculus"]
}
```

Here, `courses` is an array containing multiple course names.

## 8. Nested Documents

Nested documents allow you to represent hierarchical data structures within a single document. Let's add an `address` field for Larry.

```javascript
{
    name: "Larry Lobster",
    age: 32,
    gpa: 2.8,
    full_time: false,
    registration_date: new Date(),
    graduation_date: null,
    courses: ["biology", "chemistry", "calculus"],
    address: {
        street: "123 Fake Street",
        city: "Bikini Bottom",
        zip_code: "12345"
    }
}
```

Here, `address` is a nested document containing street, city, and zip code fields.
