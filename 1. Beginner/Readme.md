## Begginer codes you must know in MongoDB

- show dbs
- use myDatabase
- show collections
- db.myCollection.insertOne({ name: "Alice", age: 25 })
- db.myCollection.find()
- db.myCollection.find({ age: 25 })
- db.myCollection.updateOne({ name: "Alice" }, { $set: { age: 26 } })
- db.myCollection.deleteOne({ name: "Alice" })
- db.myCollection.drop()
- db.dropDatabase()









### Explanation and use :


1. show dbs: Shows all databases you have.

2. use myDatabase: Switches to the database named myDatabase. If it doesn't exist, it will be created when data is inserted.

3. db.createCollection("myCollection") : Creates a collection

3. show collections: Displays all collections within the currently selected database.

4. db.myCollection.insertOne({ name: "Alice", age: 25 }): Inserts a single document with name and age fields into the myCollection collection.

5. db.myCollection.find(): Retrieves and displays all documents in the myCollection collection.




6. db.myCollection.find({ age: 25 }): Retrieves documents from myCollection where the age field is 25.

7. db.myCollection.updateOne({ name: "Alice" }, { $set: { age: 26 } }): Updates the first document found with name "Alice", setting its age field to 26.

8. db.myCollection.deleteOne({ name: "Alice" }): Deletes the first document found in myCollection where name is "Alice".

9. db.myCollection.drop(): Removes the entire myCollection collection from the database.

10. db.dropDatabase(): Deletes the current database and all its collections and documents.