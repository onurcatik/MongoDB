## MongoDB Assignment

### Objective
This assignment aims to reinforce your understanding of MongoDB installation, basic operations, and using MongoDB with Visual Studio Code. By completing this assignment, you will gain hands-on experience in setting up MongoDB, connecting to a MongoDB instance, and performing basic CRUD (Create, Read, Update, Delete) operations.

### Part 1: Installation

1. **Visit MongoDB Website:**
   - Go to [mongodb.com](https://www.mongodb.com/).
   - Navigate to the "Resources" section and click on "Server" in the left sidebar.

2. **Select Installation Tutorial:**
   - Choose the installation tutorial based on your operating system (focus on Windows).

3. **Download MongoDB Community Edition:**
   - Scroll down to find the "Install MongoDB Community Edition" section.
   - Download the installer for Windows.
   - Save the installer to a location of your choice.

4. **Install MongoDB:**
   - Run the downloaded installer.
   - Follow the on-screen instructions, accept the license agreement, and select installation options.
   - Install MongoDB as a service and include MongoDB Compass.

5. **Install MongoDB Shell:**
   - Go to the "MongoDB Shell" section on the MongoDB website.
   - Download the appropriate version for Windows.
   - Save the installer and unzip the folder.

6. **Set up Environment Variables:**
   - Copy the path to the MongoDB Shell executable.
   - Add the file path to your system's environment variables (`MONGODB_HOME`).

### Part 2: Getting Started with MongoDB

1. **Using MongoDB Compass:**
   - Open MongoDB Compass.
   - Click the "Connect" button to establish a connection to your MongoDB instance.
   - Explore the interface to manage databases, collections, and documents.

2. **Using MongoDB Shell:**
   - Open the MongoDB Shell by typing `mongo` in your terminal or command prompt.
   - Verify the connection by typing `show dbs` to list all databases.

3. **Basic Operations:**
   - Create a new database named `testDB`: `use testDB`.
   - Create a new collection named `users`: `db.createCollection("users")`.
   - Insert a document into the `users` collection: `db.users.insertOne({ name: "Alice", age: 25 })`.
   - Query the `users` collection to find the inserted document: `db.users.find({ name: "Alice" })`.
   - Update the document: `db.users.updateOne({ name: "Alice" }, { $set: { age: 26 } })`.
   - Delete the document: `db.users.deleteOne({ name: "Alice" })`.

### Part 3: Using MongoDB Shell in Visual Studio Code

1. **Install MongoDB Extension:**
   - Open Visual Studio Code and go to the Extensions view.
   - Search for "MongoDB" and install the MongoDB extension.

2. **Connect to MongoDB:**
   - Click on the MongoDB icon in the activity bar.
   - Click on "localhost" to establish a connection to your MongoDB instance.

3. **Open MongoDB Shell:**
   - Right-click in the MongoDB extension and select "Launch MongoDB Shell."
   - Execute MongoDB commands in the integrated terminal.

### Part 4: Assignment Submission

Create a report documenting the following:

1. **Installation Process:**
   - Screenshots of each step during the MongoDB installation and setup.

2. **Basic Operations:**
   - Commands used and the output for creating the database, collection, and performing CRUD operations.
   - Screenshots of the MongoDB Compass interface showing the created `testDB` and `users` collection.

3. **Visual Studio Code Integration:**
   - Screenshots of connecting to MongoDB and performing operations using the integrated MongoDB Shell in Visual Studio Code.

### Bonus Tasks

1. **Advanced Queries:**
   - Write and execute a query to find all documents in the `users` collection where the age is greater than 20.

2. **Indexing:**
   - Create an index on the `name` field in the `users` collection and demonstrate its effect on query performance.
