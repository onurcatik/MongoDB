# Assignment: Insert Documents into MongoDB

**Objective:**
Learn to insert documents into a MongoDB database using both MongoDB Shell and MongoDB Compass. This assignment will test your understanding of basic MongoDB operations such as inserting single and multiple documents and verifying the insertion.

**Prerequisites:**

- MongoDB installed on your machine.
- Basic understanding of MongoDB concepts like databases, collections, and documents.

**Instructions:**

## Part 1: Using MongoDB Shell

1. **Set Up Your Database:**
   - Open MongoDB Shell.
   - Use the `school` database. If it doesn’t exist, MongoDB will create it for you.

     ```bash
     use school
     ```

2. **Insert a Single Document:**
   - Insert a document for a student named SpongeBob with an age of 30 and a GPA of 3.2 into the `students` collection.

     ```javascript
     db.students.insertOne({
         name: "SpongeBob",
         age: 30,
         GPA: 3.2
     })
     ```

3. **Verify the Inserted Document:**
   - Use the `find()` method to verify that the document has been inserted correctly.

     ```bash
     db.students.find()
     ```

4. **Insert Multiple Documents:**
   - Insert documents for three more students: Patrick, Sandy, and Gary.

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

5. **Verify All Documents:**
   - Use the `find()` method again to display all documents in the collection.

     ```bash
     db.students.find()
     ```

## Part 2: Using MongoDB Compass

1. **Navigate to the Correct Database and Collection:**
   - Open MongoDB Compass.
   - Ensure you are within the `school` database and `students` collection.

2. **Insert a Single Document:**
   - Click on the "Insert Document" button.
   - Enter the details of SpongeBob’s document:
     - Name: SpongeBob
     - Age: 30
     - GPA: 3.2
   - Click on the "Insert" button.

3. **Verify the Inserted Document:**
   - Navigate to the "Collection" tab and click on the "Documents" sub-tab to view the inserted document.

4. **Insert Multiple Documents:**
   - Click on the "Insert Document" button again.
   - Enter the details of the documents for Patrick, Sandy, and Gary in the provided JSON format:

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

   - Click on the "Insert" button.

5. **Verify All Documents:**
   - View all documents in the `students` collection by navigating to the "Collection" tab and clicking on the "Documents" sub-tab.

**Submission:**

- **Screenshots:**
  - MongoDB Shell: Provide screenshots showing the successful insertion and verification of documents.
  - MongoDB Compass: Provide screenshots showing the successful insertion and verification of documents.

- **Document:**
  - Create a document (PDF or Word) containing your screenshots and a brief description of each step you performed.

Ensure your screenshots are clear and all details are visible. Submit your document by uploading it to your assignment submission portal.
