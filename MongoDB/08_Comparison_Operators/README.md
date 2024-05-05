# MongoDB Comparison Operators Tutorial


In MongoDB, comparison operators allow you to query data based on specific value comparisons. These operators are denoted with the dollar sign ($) and can be used to filter documents in a collection based on various criteria. This tutorial will cover different comparison operators in MongoDB, along with code snippets for each operator.

**Comparison Operators:**

**1. Not Equals ($ne):**
The `$ne` operator is used to find documents where a specified field is not equal to a certain value.

```javascript
// Example: Find all students whose name is not "SpongeBob"
db.students.find({ name: { $ne: "SpongeBob" } });
```

**2. Less Than ($lt) and Less Than Equals To ($lte):**
The `$lt` operator is used to find documents where a specified field is less than a certain value, while `$lte` includes documents where the field is equal to the specified value.

```javascript
// Example: Find students whose age is less than 20
db.students.find({ age: { $lt: 20 } });

// Example: Find students whose age is less than or equal to 27
db.students.find({ age: { $lte: 27 } });
```

**3. Greater Than ($gt) and Greater Than Equals To ($gte):**
The `$gt` operator is used to find documents where a specified field is greater than a certain value, while `$gte` includes documents where the field is equal to the specified value.

```javascript
// Example: Find students whose age is greater than 27
db.students.find({ age: { $gt: 27 } });

// Example: Find students whose age is greater than or equal to 27
db.students.find({ age: { $gte: 27 } });
```

**4. Range Queries:**
You can use multiple comparison operators to specify a range for a field.

```javascript
// Example: Find students whose GPA is between 3 and 4
db.students.find({ GPA: { $gte: 3, $lt: 4 } });
```

**5. In Operator ($in) and Not In Operator ($nin):**
The `$in` operator is used to find documents where a field matches any value in a specified array. Conversely, the `$nin` operator is used to find documents where a field does not match any value in a specified array.

```javascript
// Example: Find students whose name is either SpongeBob, Patrick, or Sandy
db.students.find({ name: { $in: ["SpongeBob", "Patrick", "Sandy"] } });

// Example: Find students whose name is not SpongeBob, Patrick, or Sandy
db.students.find({ name: { $nin: ["SpongeBob", "Patrick", "Sandy"] } });
```

**Using Compass:**
You can also perform these queries using MongoDB Compass by typing your filter criteria in the filter text box.
