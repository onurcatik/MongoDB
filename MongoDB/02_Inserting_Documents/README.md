# MongoDB Insert Documents Tutorial

In this tutorial, we'll cover how to insert documents into a MongoDB database using both the MongoDB Shell and MongoDB Compass. We'll walk through inserting single documents as well as multiple documents using both methods. Let's dive in!

### Prerequisites:

- MongoDB installed on your machine.
- Basic understanding of MongoDB concepts like databases, collections, and documents.

### MongoDB Shell Method:

1. **Navigate to the Correct Database:**
   First, ensure that you are using the correct database. If you're following from the previous topic where the database was named "school", let's clear the screen and use that database.

   ```bash
   use school
   ```
2. **Insert Single Document:**
   To insert a single document into a collection, use the `insertOne()` method. For example, let's insert a document for a student named SpongeBob with an age of 30 and a GPA of 3.2.

   ```javascript
   db.students.insertOne({
       name: "SpongeBob",
       age: 30,
       GPA: 3.2
   })
   ```
3. **View Inserted Document:**
   To verify that the document has been inserted, you can use the `find()` method.

   ```bash
   db.students.find()
   ```
4. **Insert Multiple Documents:**
   To insert multiple documents at once, use the `insertMany()` method. Place all documents to be inserted within an array.

   ```javascript
   db.students.insertMany([
       {
           name: "Patrick",
           age: 38,
           GPA: 1.5
       },
       {
           name: "Sandy",
           age: 27,
           GPA: 4.0
       },
       {
           name: "Gary",
           age: 18,
           GPA: 2.5
       }
   ])
   ```
5. **View All Documents:**
   Use the `find()` method again to display all documents in the collection.

   ```bash
   db.students.find()
   ```

### MongoDB Compass Method:

1. **Navigate to the Correct Database and Collection:**
   Open MongoDB Compass and ensure you are within the correct database and collection where you want to insert the documents.
2. **Insert Single Document:**
   Click on the "Insert Document" button. Enter the details of the document in the provided fields. For example, for SpongeBob:

   - Name: SpongeBob
   - Age: 30
   - GPA: 3.2

   Then click on the "Insert" button.
3. **Insert Multiple Documents:**
   Click on the "Insert Document" button again. This time, to insert multiple documents, enter the details of each document separated by commas within square brackets. For example:

   ```json
   [
       {
           "name": "Patrick",
           "age": 38,
           "GPA": 1.5
       },
       {
           "name": "Sandy",
           "age": 27,
           "GPA": 4.0
       },
       {
           "name": "Gary",
           "age": 18,
           "GPA": 2.5
       }
   ]
   ```

   Then click on the "Insert" button.
4. **View All Documents:**
   After inserting the documents, you can view them in the collection by navigating to the "Collection" tab and clicking on the "Documents" sub-tab.
