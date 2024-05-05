# Creating and Managing MongoDB Databases

MongoDB is a popular NoSQL database that offers flexibility and scalability for your data storage needs. In this tutorial, we will explore how to create and manage databases using both the MongoDB Shell and MongoDB Compass.

**1. Using MongoDB Shell**

**1.1. Viewing Existing Databases:**
To view all existing databases, open the MongoDB Shell and type:

```bash
show dbs
```

This command will display a list of all current databases. You will typically see default databases like `admin`, `config`, and `local`.

**1.2. Creating a New Database:**
To create a new database, use the `use` command followed by the desired database name. For example:

```bash
use school
```

This command creates a new database named `school` and switches to it. Note that if the database doesn't exist, MongoDB will create it upon the first document insertion.

**1.3. Adding a Collection:**
To add a collection to the current database, use the `db.createCollection()` method. For instance:

```bash
db.createCollection("students")
```

This command creates a collection named `students` within the `school` database.

**1.4. Dropping a Database:**
To drop the current database, use the `db.dropDatabase()` method:

```bash
db.dropDatabase()
```

This command deletes the currently selected database. Exercise caution as this action is irreversible.

**2. Using MongoDB Compass**

**2.1. Creating a Database:**
MongoDB Compass provides a graphical user interface for MongoDB. To create a database using Compass:

- Open Compass and connect to your MongoDB server.
- Click the "Create Database" button.
- Enter the desired database name, e.g., `school`.
- Optionally, configure additional preferences.
- Click "Create Database" to finalize.

**2.2. Creating a Collection:**
To create a collection within the newly created database:

- Select the database from the sidebar.
- Click the "+" button next to "Collections".
- Enter the collection name, e.g., `students`.
- Click "Create" to confirm.

**2.3. Deleting a Database:**
To delete a database using MongoDB Compass:

- Select the database from the sidebar.
- Click the "Drop Database" button (trash can icon).
- Type the name of the database to confirm deletion.
- Click "Drop Database" to execute.
