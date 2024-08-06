## Intermediate codes you must know in MongoDB



1. db.myCollection.insertMany([{ name: "Bob", age: 30 }, { name: "Carol", age: 22 }]): Inserts multiple documents into myCollection in a single operation.

2. db.myCollection.find({}, { name: 1, _id: 0 }): Retrieves all documents from myCollection, including only the name field and excluding the _id field.

3. db.myCollection.updateMany({ age: { $lt: 30 } }, { $set: { status: "young" } }): Updates all documents in myCollection where age is less than 30, setting the status field to "young".

4. db.myCollection.deleteMany({ status: "young" }): Deletes all documents from myCollection where the status field is "young".

5. db.myCollection.createIndex({ name: 1 }): Creates an ascending index on the name field in myCollection to improve query performance.

























6. db.myCollection.getIndexes(): Lists all indexes currently on the myCollection collection.

7. db.myCollection.aggregate([{ $match: { age: { $gt: 20 } } }, { $group: { _id: "$age", count: { $sum: 1 } } }]): Uses aggregation to filter documents where age is greater than 20 and group them by age, counting the number of documents in each group.

8. db.myCollection.find().sort({ age: -1 }): Retrieves documents from myCollection and sorts them by the age field in descending order.

9. db.myCollection.aggregate([{ $match: { age: { $gte: 20 } } }, { $group: { _id: "$age", total: { $sum: 1 }, avgAge: { $avg: "$age" } } }, { $sort: { avgAge: -1 } }]): Performs a complex aggregation to filter documents where age is at least 20, group by age, calculate the total and average age, and sort by average age in descending order.

10. db.orders.aggregate([{ $lookup: { from: "products", localField: "productId", foreignField: "_id", as: "productDetails" } }]): Uses $lookup to join documents from orders with related documents from products based on the productId field.























11. db.myCollection.createIndex({ description: "text" }): Creates a text index on the description field to enable full-text search.

12. db.myCollection.find({ $text: { $search: "MongoDB" } }): Performs a full-text search for documents in myCollection where the description field contains the term "MongoDB".

13. rs.initiate(): Initializes a replica set, which sets up primary and secondary nodes for data replication.

14. rs.add("hostname:port"): Adds a new secondary node to the replica set.

15. sh.enableSharding("myDatabase"): Enables sharding for the myDatabase database, allowing it to be distributed across multiple servers.





















16. db.myCollection.createIndex({ _id: 1 }): Creates a shard key index on the _id field for sharding purposes.

17. sh.shardCollection("myDatabase.myCollection", { _id: "hashed" }): Shards the myCollection collection in myDatabase using a hashed distribution on the _id field.

18. const changeStream = db.myCollection.watch(); changeStream.on("change", (change) => { console.log("Change detected:", change) }): Creates a change stream to listen for and log real-time changes in myCollection.

19. db.createCollection("myCollection", { validator: { $jsonSchema: { bsonType: "object", required: [ "name", "age" ], properties: { name: { bsonType: "string", description: "Name must be a string" }, age: { bsonType: "int", minimum: 0, maximum: 120, description: "Age must be an integer between 0 and 120" } } } } }): Creates a collection with schema validation, ensuring documents must have name and age fields with specific types and constraints.