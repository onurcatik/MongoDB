# MongoDB Sorting and Limiting Tutorial

MongoDB offers powerful capabilities for sorting and limiting documents, allowing you to efficiently manage and retrieve data from your collections. In this tutorial, we'll delve into how to use MongoDB's sorting and limiting features effectively.

### 1. Introduction to Sorting and Limiting in MongoDB

Sorting and limiting are essential operations in MongoDB when you want to retrieve specific documents from a collection in a particular order and limit the number of documents returned. MongoDB provides methods like `sort()` and `limit()` to accomplish these tasks.

### 2. Sorting Documents

To sort documents in MongoDB, you can use the `sort()` method in conjunction with the `find()` method. Let's go through the process step by step:

#### Sorting by a Field

```javascript
// Sorting documents by 'Name' field in alphabetical order
DB.students.find().sort({Name: 1});
```

This query retrieves all documents from the 'students' collection and sorts them by the 'Name' field in ascending alphabetical order.

```javascript
// Sorting documents by 'GPA' field in descending order
DB.students.find().sort({GPA: -1});
```

Here, we're sorting documents by the 'GPA' field in descending order, from highest to lowest.

### 3. Limiting Documents

Limiting documents allows you to control the number of documents returned in a query. MongoDB's `limit()` method facilitates this functionality.

```javascript
// Limiting the number of returned documents to 1
DB.students.find().limit(1);
```

This query limits the number of returned documents to 1, which can be useful when you only need a single result.

```javascript
// Limiting the number of returned documents to 3
DB.students.find().limit(3);
```

Here, we limit the returned documents to 3, useful for scenarios where you want to retrieve a subset of results.

### 4. Combining Sorting and Limiting

You can also combine sorting and limiting to refine your queries further.

```javascript
// Sorting documents by GPA in descending order and limiting to 1
DB.students.find().sort({GPA: -1}).limit(1);
```

This query sorts documents by GPA in descending order and then limits the result to 1, effectively retrieving the document with the highest GPA.

```javascript
// Sorting documents by GPA in ascending order and limiting to 1
DB.students.find().sort({GPA: 1}).limit(1);
```

Similarly, this query sorts documents by GPA in ascending order and limits the result to 1, returning the document with the lowest GPA.
