# Deleting Documents in MongoDB

MongoDB is a powerful NoSQL database that allows for flexible data storage and retrieval. One common operation when working with MongoDB is deleting documents from collections. In this tutorial, we'll explore various methods to delete documents using both MongoDB Compass and the MongoDB Shell.

## Exporting Your Collection (Optional)

Before performing any deletions, it's a good practice to export your collection. This serves as a backup in case you accidentally delete important data. Here's how to export your collection using MongoDB Compass:

1. Open MongoDB Compass.
2. Select your database and collection.
3. Click on the "Export" button.
4. Choose the export format (JSON or CSV).
5. Specify the destination for the exported file.
6. Click "Export."

## Deleting Documents in MongoDB Compass

Deleting documents in MongoDB Compass is straightforward. Follow these steps:

1. Open MongoDB Compass.
2. Select your database and collection.
3. Locate the document you want to delete.
4. Click on the trash can icon next to the document.
5. Confirm the deletion.

## Deleting Documents in MongoDB Shell

Deleting documents using the MongoDB Shell provides more flexibility and power. Here's how to do it:

1. Open your MongoDB Shell.
2. Select the database where your collection resides using the `use` command.

   ```
   use your_database_name
   ```
3. To delete a single document, use the `deleteOne` method:

   ```
   db.your_collection_name.deleteOne({ criteria })
   ```

   Replace `{ criteria }` with the filter criteria for the document you want to delete.

   Example:

   ```
   db.students.deleteOne({ name: "Larry" })
   ```
4. To delete multiple documents matching a criteria, use the `deleteMany` method:

   ```
   db.your_collection_name.deleteMany({ criteria })
   ```

   Replace `{ criteria }` with the filter criteria for the documents you want to delete.

   Example:

   ```
   db.students.deleteMany({ full_time: false })
   ```
5. You can also delete documents based on the absence or presence of a field:

   - To delete documents where a field does not exist:
     ```
     db.your_collection_name.deleteMany({ field: { $exists: false } })
     ```
   - To delete documents where a field exists:
     ```
     db.your_collection_name.deleteMany({ field: { $exists: true } })
     ```
6. After deleting documents, you can verify the changes using the `find` method:

   ```
   db.your_collection_name.find()
   ```

## Importing Your Collection

Once you've completed the deletions, you may want to import your previously exported collection back into MongoDB. Here's how to do it using MongoDB Compass:

1. Open MongoDB Compass.
2. Select your database.
3. Click on "Add Data" and choose "Import JSON or CSV file."
4. Locate your exported file and import it into the database.
