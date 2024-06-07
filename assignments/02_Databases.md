# Assignment: Creating and Managing MongoDB Databases

This assignment is designed to help you practice creating and managing MongoDB databases using both the MongoDB Shell and MongoDB Compass. Follow the instructions provided to complete the tasks. Submit your MongoDB commands and screenshots where applicable.

## Part 1: Using MongoDB Shell

1. **Viewing Existing Databases**
   - Open the MongoDB Shell.
   - Execute the command to list all existing databases.
   - **Command:**

     ```bash
     show dbs
     ```

   - **Submission:** Take a screenshot showing the output of the `show dbs` command.

2. **Creating a New Database**
   - Create a new database named `university`.
   - **Command:**

     ```bash
     use university
     ```

   - **Submission:** Provide the command used and take a screenshot showing that you have switched to the `university` database.

3. **Adding a Collection**
   - Add a collection named `courses` to the `university` database.
   - **Command:**

     ```bash
     db.createCollection("courses")
     ```

   - **Submission:** Provide the command used and take a screenshot showing the creation of the `courses` collection.

4. **Dropping a Database**
   - Drop the `university` database.
   - **Command:**

     ```bash
     db.dropDatabase()
     ```

   - **Submission:** Provide the command used and take a screenshot showing that the `university` database has been dropped.

## Part 2: Using MongoDB Compass

1. **Creating a Database**
   - Open MongoDB Compass and connect to your MongoDB server.
   - Create a new database named `library`.
   - **Instructions:**
     - Click the "Create Database" button.
     - Enter the database name `library`.
     - Click "Create Database".
   - **Submission:** Take a screenshot of the database creation process and the final screen showing the `library` database.

2. **Creating a Collection**
   - Create a collection named `books` within the `library` database.
   - **Instructions:**
     - Select the `library` database from the sidebar.
     - Click the "+" button next to "Collections".
     - Enter the collection name `books`.
     - Click "Create".
   - **Submission:** Take a screenshot showing the creation of the `books` collection within the `library` database.

3. **Deleting a Database**
   - Delete the `library` database.
   - **Instructions:**
     - Select the `library` database from the sidebar.
     - Click the "Drop Database" button (trash can icon).
     - Type `library` to confirm the deletion.
     - Click "Drop Database".
   - **Submission:** Take a screenshot showing the deletion process and the confirmation of the database being dropped.
