# Updating Documents in MongoDB

In MongoDB, updating documents is a common operation when managing data. Whether you need to modify one document or multiple documents, MongoDB provides flexible methods to accomplish this task. In this tutorial, we'll explore how to update documents using both the MongoDB Shell and MongoDB Compass. We'll cover updating single documents (`updateOne`) and multiple documents (`updateMany`), along with various operators like `$set` and `$unset`.

**Updating Documents in MongoDB Shell:**

1. **Updating a Single Document (`updateOne`):**

   To update a single document, we use the `updateOne` method. Let's say we have a collection named `students`, and we want to update the name of a student named SpongeBob.

   ```javascript
   db.students.updateOne(
       { name: "SpongeBob" }, // Filter
       { $set: { full_time: true } } // Update parameter
   );
   ```

   - In the first parameter, we provide the filter criteria to identify the document(s) to update.
   - In the second parameter, we use the `$set` operator to specify the changes to be made.
2. **Updating by Object ID:**

   To ensure uniqueness, we can update documents based on their Object ID.

   ```javascript
   db.students.updateOne(
       { _id: ObjectId("your_object_id_here") }, // Filter by Object ID
       { $set: { full_time: false } } // Update parameter
   );
   ```

   - Replace `"your_object_id_here"` with the actual Object ID of the document you want to update.
3. **Removing a Field (`$unset` operator):**

   If we want to remove a field from a document, we use the `$unset` operator.

   ```javascript
   db.students.updateOne(
       { name: "SpongeBob" }, // Filter
       { $unset: { full_time: "" } } // Remove the full_time field
   );
   ```

   - This will remove the `full_time` field from the document.
4. **Updating Multiple Documents (`updateMany`):**

   We can update multiple documents at once using the `updateMany` method.

   ```javascript
   db.students.updateMany(
       {}, // Empty filter to select all documents
       { $set: { full_time: false } } // Update parameter
   );
   ```

   - Here, we set `full_time` to `false` for all documents.
5. **Checking Updates:**

   After executing update commands, you can verify the changes using the `find` method.

   ```javascript
   db.students.find();
   ```

   - This will display all documents in the `students` collection with their updated fields.

**Updating Documents in MongoDB Compass:**

1. **Editing Documents:**

   - Open MongoDB Compass and navigate to the collection containing the document(s) you want to update.
   - Click on the pencil icon to edit the document.
   - To remove a field, click the trash can icon next to the field name.
   - To add a field, click the pencil icon again and then the plus button to add a new field.
2. **Changing Values:**

   - To change the value of a field, select the field and modify its value.
   - You can also change the data type of a field if needed.
3. **Saving Changes:**

   - After making the desired updates, click the update/save button to save the changes to the document.
