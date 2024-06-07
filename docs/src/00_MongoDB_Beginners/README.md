# MongoDB Tutorial for Beginners 🍃

MongoDB is a NoSQL database management system that has gained immense popularity due to its ability to handle large volumes of data efficiently. Unlike traditional relational database management systems (RDBMS), MongoDB stores data in a flexible, schema-less format, making it suitable for a wide range of applications. In this comprehensive tutorial, we will cover everything you need to know to get started with MongoDB in about an hour.

## Prerequisites

Before diving into MongoDB, make sure you have the following prerequisites:

- Basic understanding of an object-oriented programming language (e.g., Python, Java, C++, JavaScript).

## Installation

Let's begin by installing MongoDB on your system.

1. **Visit MongoDB Website:**

   - Go to [mongodb.com](https://www.mongodb.com/).
   - Navigate to the "Resources" section and click on "Server" in the left sidebar.
2. **Select Installation Tutorial:**

   - Choose the installation tutorial based on your operating system. For this tutorial, we'll focus on the Windows platform.
3. **Download MongoDB Community Edition:**

   - Scroll down to find the "Install MongoDB Community Edition" section.
   - Follow the instructions to download the installer for your platform (in this case, Windows).
   - Save the installer to a location of your choice.
4. **Install MongoDB:**

   - Run the downloaded installer.
   - Follow the on-screen instructions, accepting the license agreement and selecting installation options.
   - Make sure to install MongoDB as a service and include MongoDB Compass, a graphical user interface for managing MongoDB databases.
5. **Install MongoDB Shell:**

   - After installing MongoDB, proceed to install the MongoDB Shell.
   - Again, go to the left sidebar on the MongoDB website and select "MongoDB Shell."
   - Download the appropriate version for your platform (Windows in this case).
   - Save the installer and unzip the folder.
6. **Set up Environment Variables:**

   - Copy the path to the MongoDB Shell executable.
   - Add the file path to your system's environment variables:
     - Search for "environment variables" in your system settings.
     - Under "System Variables," click on "New" and add a variable name (e.g., `MONGODB_HOME`) with the MongoDB Shell executable path.
     - Click "OK" to save the changes.

## Getting Started with MongoDB

Now that MongoDB is installed, let's explore how to connect to the database and perform basic operations.

1. **Using MongoDB Compass:**

   - Open MongoDB Compass from the desktop shortcut or start menu.
   - Click the "Connect" button to establish a connection to your MongoDB instance.
   - MongoDB Compass provides a graphical interface for managing databases, collections, and documents.
2. **Using MongoDB Shell:**

   - Open the MongoDB Shell by typing `mongo` in your terminal or command prompt.
   - You can also use Visual Studio Code with the MongoDB extension for a more integrated experience.
3. **Connecting to MongoDB:**

   - To establish a connection to your MongoDB instance, type `mongo` or `sh` in the terminal.
   - You should see a prompt indicating a successful connection.
4. **Basic Operations:**

   - Once connected, you can perform various operations such as creating databases, collections, inserting documents, querying data, and more.
   - Use commands like `db.createCollection()`, `db.collection.insertOne()`, `db.collection.find()`, etc., to interact with the database.
5. **Exiting MongoDB Shell:**

   - To exit the MongoDB Shell, type `exit` and press Enter.

## Using MongoDB Shell in Visual Studio Code

If you prefer using Visual Studio Code for MongoDB development, follow these steps:

1. **Install MongoDB Extension:**

   - Open Visual Studio Code and go to the Extensions view.
   - Search for "MongoDB" and install the MongoDB extension.
2. **Connect to MongoDB:**

   - Click on the MongoDB icon in the activity bar.
   - Click on "localhost" to establish a connection to your MongoDB instance.
3. **Open MongoDB Shell:**

   - Right-click in the MongoDB extension and select "Launch MongoDB Shell."
   - This will open a terminal integrated within Visual Studio Code for interacting with MongoDB.
4. **Perform Operations:**

   - Use the integrated terminal to execute MongoDB commands just like you would in the standalone MongoDB Shell.
5. **Exit MongoDB Shell:**

   - To exit the MongoDB Shell, type `exit` and press Enter.
