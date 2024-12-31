## Technology Docs

- [Angular](Angular.md)  
- [MongoDB](MongoDB.md)  
- [MySQL](Mysql.md)  
- [Node.js](Node-Js.md)  
- [TypeScript](TypeScript.md)  
- [JavaScript](JavaScript.md)
Here’s a list of 100+ MongoDB interview questions and answers with examples that could help in preparation for your interviews. I'll split them into sections, each focused on different aspects of MongoDB.

### 1. **Basics of MongoDB**

**Q1. What is MongoDB?**

**Answer:**
MongoDB is a NoSQL database that provides high performance, high availability, and easy scalability. It uses a document-oriented data model, where data is stored in JSON-like format (BSON).

---

**Q2. What is BSON?**

**Answer:**
BSON (Binary JSON) is a binary representation of JSON-like documents. It is used to store data in MongoDB and supports more data types than JSON, such as `ObjectId`, `Date`, and others.

---

**Q3. How is MongoDB different from traditional relational databases?**

**Answer:**
- MongoDB is schema-less (flexible schema) while relational databases use a fixed schema.
- MongoDB uses collections and documents instead of tables and rows.
- MongoDB supports horizontal scaling and sharding, whereas relational databases typically use vertical scaling.

---

**Q4. What is a MongoDB document?**

**Answer:**
A MongoDB document is a basic unit of data in MongoDB, represented in BSON format. It is similar to a JSON object with key-value pairs.

```json
{
  "_id": ObjectId("60d5f2a3c1c8c7f5c88f24ab"),
  "name": "Alice",
  "age": 28
}
```

---

**Q5. What is a MongoDB collection?**

**Answer:**
A MongoDB collection is a group of documents. It is analogous to a table in a relational database. A collection does not enforce any schema for the documents within it.

```js
db.users.insertOne({ name: "Alice", age: 28 });
```

---

### 2. **CRUD Operations**

**Q6. How do you create a document in MongoDB?**

**Answer:**
You can create a document using the `insertOne()` or `insertMany()` methods.

```js
db.users.insertOne({ name: "Alice", age: 28 });
```

---

**Q7. How do you read data in MongoDB?**

**Answer:**
You can read data using the `find()` method.

```js
db.users.find({ age: { $gt: 20 } });
```

---

**Q8. How do you update a document in MongoDB?**

**Answer:**
You can update a document using the `updateOne()`, `updateMany()`, or `replaceOne()` methods.

```js
db.users.updateOne(
  { name: "Alice" },
  { $set: { age: 29 } }
);
```

---

**Q9. How do you delete a document in MongoDB?**

**Answer:**
You can delete a document using the `deleteOne()` or `deleteMany()` methods.

```js
db.users.deleteOne({ name: "Alice" });
```

---

### 3. **Operators**

**Q10. What is the `$gt` operator in MongoDB?**

**Answer:**
The `$gt` operator is used to match values greater than a specified value.

```js
db.users.find({ age: { $gt: 25 } });
```

---

**Q11. What is the `$set` operator in MongoDB?**

**Answer:**
The `$set` operator is used to update the value of a field in a document.

```js
db.users.updateOne({ name: "Alice" }, { $set: { age: 30 } });
```

---

**Q12. What is the `$in` operator in MongoDB?**

**Answer:**
The `$in` operator is used to match values that are in a specified array.

```js
db.users.find({ age: { $in: [25, 28, 30] } });
```

---

### 4. **Indexes**

**Q13. What is an index in MongoDB?**

**Answer:**
An index is a data structure that improves the speed of data retrieval operations on a collection.

---

**Q14. How do you create an index in MongoDB?**

**Answer:**
You can create an index using the `createIndex()` method.

```js
db.users.createIndex({ name: 1 });
```

---

**Q15. What is the difference between ascending and descending indexes?**

**Answer:**
- Ascending index (`1`): Sorts the indexed field in ascending order.
- Descending index (`-1`): Sorts the indexed field in descending order.

---

### 5. **Aggregation Framework**

**Q16. What is the Aggregation Framework in MongoDB?**

**Answer:**
The Aggregation Framework is used to perform operations such as filtering, grouping, and sorting on documents within a collection. It consists of stages like `$match`, `$group`, `$sort`, and others.

---

**Q17. How do you use the `$group` operator in MongoDB?**

**Answer:**
The `$group` operator is used to group documents by a specified identifier and perform aggregation operations.

```js
db.orders.aggregate([
  { $group: { _id: "$customer_id", total: { $sum: "$amount" } } }
]);
```

---

**Q18. How do you use the `$match` operator in MongoDB?**

**Answer:**
The `$match` operator is used to filter documents based on the specified criteria.

```js
db.orders.aggregate([
  { $match: { status: "shipped" } }
]);
```

---

### 6. **Replication**

**Q19. What is replication in MongoDB?**

**Answer:**
Replication is the process of synchronizing data across multiple MongoDB servers to ensure high availability and redundancy. It is achieved through replica sets.

---

**Q20. What is a replica set in MongoDB?**

**Answer:**
A replica set is a group of MongoDB instances that maintain the same data set. It consists of a primary node and multiple secondary nodes.

---

**Q21. How do you configure replication in MongoDB?**

**Answer:**
To configure replication, you initiate a replica set by connecting to the MongoDB instance and running the `rs.initiate()` command.

```js
rs.initiate();
```

---

### 7. **Sharding**

**Q22. What is sharding in MongoDB?**

**Answer:**
Sharding is a method used to distribute data across multiple servers, allowing MongoDB to horizontally scale.

---

**Q23. How does sharding work in MongoDB?**

**Answer:**
Sharding works by dividing data into chunks and distributing them across multiple shards based on a shard key.

---

### 8. **Security**

**Q24. How do you enable authentication in MongoDB?**

**Answer:**
To enable authentication, you need to configure the `security.authorization` option in the MongoDB configuration file (`mongod.conf`).

```yaml
security:
  authorization: "enabled"
```

---

**Q25. What is Role-Based Access Control (RBAC) in MongoDB?**

**Answer:**
RBAC is a system where users are assigned specific roles with certain permissions that control access to database resources.

---

### 9. **Backup and Restore**

**Q26. How do you backup MongoDB data?**

**Answer:**
You can back up MongoDB data using the `mongodump` command.

```bash
mongodump --out /path/to/backup
```

---

**Q27. How do you restore MongoDB data?**

**Answer:**
You can restore MongoDB data using the `mongorestore` command.

```bash
mongorestore /path/to/backup
```

Here are more MongoDB interview questions, answers, and examples to help you with your preparation.

### 10. **Data Modeling**

**Q28. What is a reference vs. an embedded document in MongoDB?**

**Answer:**
- **Reference**: One document stores a reference to another document (similar to foreign keys in relational databases).
- **Embedded Document**: One document stores the entire content of another document as a sub-document.

**Example:**
- **Reference**: 
    ```js
    db.orders.insertOne({
      order_id: 1,
      customer_id: ObjectId("60d5f2a3c1c8c7f5c88f24ab"),
      total: 100
    });
    ```
- **Embedded**:
    ```js
    db.orders.insertOne({
      order_id: 1,
      customer: { name: "Alice", address: "123 Street" },
      total: 100
    });
    ```

---

**Q29. What are the advantages and disadvantages of embedding documents?**

**Answer:**
- **Advantages**:
    - Faster reads as all data is in one document.
    - Reduced complexity, as there are no joins.
- **Disadvantages**:
    - Can result in large documents that exceed MongoDB's document size limit.
    - Difficult to maintain if the embedded data is frequently updated.

---

**Q30. What are the advantages and disadvantages of using references?**

**Answer:**
- **Advantages**:
    - Keeps documents small and manageable.
    - More flexibility as data can be updated independently.
- **Disadvantages**:
    - Requires additional queries or joins (with `$lookup`).
    - Slower performance on reads if references are too deeply nested.

---

### 11. **Aggregation Pipeline**

**Q31. What are the stages in an aggregation pipeline?**

**Answer:**
The aggregation pipeline consists of multiple stages, where each stage transforms the documents as they pass through the pipeline. Some common stages include:
- `$match`: Filters documents.
- `$group`: Groups documents by a specified identifier.
- `$sort`: Sorts documents.
- `$project`: Reshapes documents.
- `$unwind`: Deconstructs an array field into multiple documents.

---

**Q32. How do you use `$unwind` in the aggregation pipeline?**

**Answer:**
The `$unwind` stage deconstructs an array field from the input documents to output a document for each element.

**Example:**
```js
db.orders.aggregate([
  { $unwind: "$items" },
  { $group: { _id: "$items.product_id", total: { $sum: "$items.quantity" } } }
]);
```

---

**Q33. What is the `$lookup` stage in aggregation, and how is it used?**

**Answer:**
The `$lookup` stage performs a left outer join to a specified collection and returns documents from the target collection.

**Example:**
```js
db.orders.aggregate([
  {
    $lookup: {
      from: "products",
      localField: "product_id",
      foreignField: "_id",
      as: "product_details"
    }
  }
]);
```

---

### 12. **Performance Optimization**

**Q34. How do you improve the performance of MongoDB queries?**

**Answer:**
- **Use indexes** to speed up queries.
- **Optimize the aggregation pipeline** by reducing stages that process large volumes of data.
- **Limit the amount of data returned** by using projection to return only necessary fields.
- **Shard large collections** to distribute data across multiple servers.

---

**Q35. What is compound indexing in MongoDB?**

**Answer:**
A compound index is an index on multiple fields in a collection. It is useful when querying multiple fields together.

**Example:**
```js
db.users.createIndex({ age: 1, name: 1 });
```
This index helps when queries use both `age` and `name` fields.

---

**Q36. How can you check the performance of a query in MongoDB?**

**Answer:**
You can use the `explain()` method to analyze query performance.

**Example:**
```js
db.users.find({ age: { $gt: 20 } }).explain("executionStats");
```

---

### 13. **Transactions**

**Q37. What are transactions in MongoDB?**

**Answer:**
Transactions allow multiple operations to be executed as a single unit, ensuring atomicity. MongoDB supports multi-document ACID transactions starting from version 4.0.

---

**Q38. How do you use transactions in MongoDB?**

**Answer:**
Transactions in MongoDB are used with `session` objects. A session starts a transaction, and the changes can be committed or aborted.

**Example:**
```js
const session = client.startSession();

session.startTransaction();
try {
  db.orders.insertOne({ customer: "Alice", total: 100 }, { session });
  db.users.updateOne({ name: "Alice" }, { $inc: { balance: -100 } }, { session });
  session.commitTransaction();
} catch (error) {
  session.abortTransaction();
  throw error;
} finally {
  session.endSession();
}
```

---

### 14. **Data Integrity**

**Q39. How do you enforce data integrity in MongoDB?**

**Answer:**
While MongoDB does not have foreign key constraints like relational databases, data integrity can be enforced using:
- **Schema Validation**: Define validation rules using MongoDB’s schema validation feature.
- **Atomic Operations**: Use transactions to ensure multiple operations are completed successfully.

---

**Q40. What is schema validation in MongoDB?**

**Answer:**
Schema validation allows you to define rules for the documents in a collection (e.g., field types, required fields, etc.).

**Example:**
```js
db.createCollection("users", {
  validator: {
    $jsonSchema: {
      bsonType: "object",
      required: ["name", "age"],
      properties: {
        name: { bsonType: "string" },
        age: { bsonType: "int" }
      }
    }
  }
});
```

---

### 15. **Backup and Recovery**

**Q41. What is a replica set in MongoDB, and how does it help in data backup?**

**Answer:**
A replica set is a group of MongoDB servers that maintain the same data set, providing redundancy and data availability. The primary node is used for reads and writes, while secondary nodes replicate the data from the primary. If the primary fails, one of the secondaries is automatically promoted to primary.

---

**Q42. How do you back up a MongoDB replica set?**

**Answer:**
You can back up a replica set using the `mongodump` command. It will back up the data from the primary node and include data from all secondaries as well.

**Example:**
```bash
mongodump --host replicaSetPrimary --out /backup/location
```

---

### 16. **Data Scaling**

**Q43. What is sharding in MongoDB, and why is it important?**

**Answer:**
Sharding is the process of distributing data across multiple servers or clusters. It is important for horizontal scaling, which allows MongoDB to handle large datasets and high-throughput applications.

---

**Q44. What is a shard key in MongoDB?**

**Answer:**
A shard key is the field or set of fields used to distribute data across shards in a MongoDB cluster. The choice of shard key can significantly impact the performance and distribution of data.

**Example:**
```js
db.orders.createIndex({ customer_id: 1 });
```
You can use `customer_id` as the shard key for distributing orders across different shards.

---

### 17. **MongoDB Atlas**

**Q45. What is MongoDB Atlas?**

**Answer:**
MongoDB Atlas is a fully managed cloud service for MongoDB, providing automated backups, scalability, and security features.

---

**Q46. How do you connect to a MongoDB Atlas cluster?**

**Answer:**
To connect to MongoDB Atlas, you need to create a cluster and use the connection string provided by Atlas.

**Example:**
```bash
mongo "mongodb+srv://cluster0.mongodb.net/myFirstDatabase" --username myUser
```

---

Here are more MongoDB interview questions, answers, and examples:

### 18. **Advanced MongoDB Features**

**Q47. What is the `$text` index in MongoDB?**

**Answer:**
The `$text` index is used for text search within MongoDB. It allows you to search for words or phrases in string fields.

**Example:**
```js
db.books.createIndex({ title: "text", author: "text" });

db.books.find({ $text: { $search: "MongoDB" } });
```
This query will search for documents where the `title` or `author` fields contain the word "MongoDB".

---

**Q48. How does MongoDB handle case sensitivity in queries?**

**Answer:**
MongoDB queries are case-sensitive by default. You can perform case-insensitive queries by using regular expressions or `$regex` with the `i` option.

**Example:**
```js
db.users.find({ name: { $regex: /^alice$/i } });
```
This query will find documents with `name` equal to "Alice", "alice", "ALICE", etc.

---

**Q49. What is a capped collection in MongoDB?**

**Answer:**
A capped collection is a fixed-size collection that automatically overwrites the oldest documents when it reaches its size limit. Capped collections are useful for logging or real-time data storage.

**Example:**
```js
db.createCollection("logs", { capped: true, size: 100000 });
```
This creates a capped collection named `logs` with a size limit of 100,000 bytes.

---

**Q50. What is the `distinct()` method in MongoDB?**

**Answer:**
The `distinct()` method returns an array of distinct values for a given field across a collection.

**Example:**
```js
db.users.distinct("age");
```
This will return an array of all unique ages from the `users` collection.

---

### 19. **Performance Tuning**

**Q51. What is the role of `explain()` in query optimization?**

**Answer:**
The `explain()` method provides information about the query execution plan, which can help identify performance bottlenecks and optimize queries.

**Example:**
```js
db.users.find({ age: { $gt: 25 } }).explain("executionStats");
```
This will show the query execution plan, including how many documents were scanned, how many index scans occurred, and whether the query used an index.

---

**Q52. What are the types of indexes available in MongoDB?**

**Answer:**
MongoDB supports several types of indexes, including:
- **Single Field Index**: Index on a single field.
- **Compound Index**: Index on multiple fields.
- **Geospatial Index**: Index for spatial data.
- **Text Index**: Index for text search.
- **Hashed Index**: Used for sharding and hash-based indexing.
- **Wildcard Index**: Indexes all fields in a document.

---

**Q53. How can you prevent index bloat in MongoDB?**

**Answer:**
Index bloat occurs when an index becomes unnecessarily large, affecting query performance. To prevent index bloat:
- Regularly review and remove unused indexes.
- Use the `background: true` option for index creation to minimize locking during index creation.
- Monitor and optimize query patterns to ensure indexes are being used effectively.

---

### 20. **Data Consistency and Reliability**

**Q54. What is write concern in MongoDB?**

**Answer:**
Write concern specifies the level of acknowledgment requested from MongoDB for write operations. It controls how many nodes in a replica set must acknowledge the write.

**Example:**
```js
db.users.insertOne({ name: "Alice" }, { writeConcern: { w: "majority" } });
```
This ensures that the write is acknowledged by the majority of the replica set nodes before being considered successful.

---

**Q55. What is read concern in MongoDB?**

**Answer:**
Read concern specifies the consistency and isolation level of read operations in MongoDB. It determines how "fresh" the data is returned from replica sets or sharded clusters.

- **local**: Returns data as it is on the node, even if not fully replicated.
- **majority**: Returns data that has been acknowledged by the majority of replica set members.
- **linearizable**: Ensures the most recent data is returned after all writes are acknowledged.

---

**Q56. How do you ensure that a MongoDB write operation is atomic?**

**Answer:**
MongoDB ensures atomicity for operations on a single document by default. If you are updating multiple documents, you can use transactions (for multi-document operations) to ensure atomicity.

**Example (Atomic Update):**
```js
db.users.updateOne(
  { _id: ObjectId("60d5f2a3c1c8c7f5c88f24ab") },
  { $set: { age: 29 } }
);
```
This update is atomic because it only affects a single document.

---

### 21. **Advanced Data Types**

**Q57. How do you store and query date/time values in MongoDB?**

**Answer:**
MongoDB uses the `Date` BSON type to store date and time values. You can query dates using the standard comparison operators.

**Example:**
```js
db.events.insertOne({ event: "Birthday", date: new Date("2024-12-31T00:00:00Z") });

db.events.find({ date: { $gte: new Date("2024-01-01T00:00:00Z") } });
```

---

**Q58. What is the `ObjectId` data type in MongoDB?**

**Answer:**
`ObjectId` is the default value for the `_id` field in MongoDB documents. It is a 12-byte identifier that is generated automatically by MongoDB and includes information about the timestamp and machine.

**Example:**
```js
const newId = new ObjectId();
db.users.insertOne({ _id: newId, name: "Bob" });
```

---

**Q59. How do you store binary data in MongoDB?**

**Answer:**
MongoDB provides the `BinData` type for storing binary data, such as images, files, or other non-text data.

**Example:**
```js
const buffer = new Buffer("binary data here");
db.files.insertOne({ data: new BinData(0, buffer) });
```

---

### 22. **Data Import and Export**

**Q60. How do you import data into MongoDB?**

**Answer:**
You can import data into MongoDB using the `mongoimport` tool, which allows you to import data from JSON, CSV, or TSV files.

**Example:**
```bash
mongoimport --db mydb --collection users --file users.json --jsonArray
```

---

**Q61. How do you export data from MongoDB?**

**Answer:**
You can export data from MongoDB using the `mongoexport` tool to export to JSON, CSV, or TSV files.

**Example:**
```bash
mongoexport --db mydb --collection users --out users.json
```

---

### 23. **MongoDB in Cloud**

**Q62. How do you connect to a MongoDB database hosted on MongoDB Atlas?**

**Answer:**
To connect to MongoDB Atlas, you need to obtain the connection string from your Atlas dashboard. You can use this connection string in your application.

**Example:**
```bash
mongo "mongodb+srv://cluster0.mongodb.net/mydatabase" --username myUser
```

---

**Q63. How does MongoDB handle automatic failover?**

**Answer:**
MongoDB handles automatic failover through replica sets. If the primary node fails, one of the secondary nodes is automatically promoted to primary without manual intervention, ensuring high availability.

---

### 24. **Miscellaneous**

**Q64. What is the `db.currentOp()` command used for in MongoDB?**

**Answer:**
The `db.currentOp()` command returns information about ongoing operations, such as running queries, locks, and background tasks. It is useful for monitoring.

**Example:**
```js
db.currentOp();
```

---

**Q65. How do you perform a bulk operation in MongoDB?**

**Answer:**
MongoDB supports bulk operations using the `bulkWrite()` method, which allows you to perform multiple write operations in a single call.

**Example:**
```js
db.users.bulkWrite([
  { insertOne: { document: { name: "Alice", age: 28 } } },
  { updateOne: { filter: { name: "Bob" }, update: { $set: { age: 32 } } } }
]);
```

Here are additional MongoDB interview questions, answers, and examples:

### 25. **Replication and Sharding**

**Q66. What is a replica set in MongoDB, and what are its components?**

**Answer:**
A **replica set** is a group of MongoDB servers that maintain the same data set, providing redundancy and high availability. It consists of the following components:
- **Primary**: Handles all write operations.
- **Secondary**: Copies data from the primary and can serve read operations.
- **Arbiter**: A member that doesn't store data but participates in elections to choose a new primary.

**Example:**
```js
db.createCollection("users", { writeConcern: { w: "majority" } });
```

---

**Q67. How does MongoDB handle elections in a replica set?**

**Answer:**
When a primary node fails, MongoDB uses a consensus algorithm to elect a new primary. An election process is triggered, and the replica set members vote to determine which secondary should become the primary.

---

**Q68. What is the difference between `writeConcern` and `readConcern`?**

**Answer:**
- **writeConcern**: Specifies the level of acknowledgment requested from MongoDB for write operations. It controls how many nodes must acknowledge the write operation before it is considered successful.
- **readConcern**: Specifies the consistency and isolation level of read operations, controlling how "fresh" the data is when read.

**Example (Write Concern):**
```js
db.users.insertOne({ name: "Alice" }, { writeConcern: { w: "majority" } });
```
This ensures the write is acknowledged by the majority of replica set members.

**Example (Read Concern):**
```js
db.users.find({}).readConcern("majority");
```
This ensures the data is returned only after the write has been acknowledged by the majority of the replica set.

---

**Q69. What is sharding in MongoDB, and how does it work?**

**Answer:**
Sharding is the process of distributing data across multiple servers, called shards, in a MongoDB cluster. It is used to horizontally scale MongoDB to handle large datasets and high throughput. Data is distributed using a **shard key**, and each shard holds a subset of the data.

---

**Q70. How does MongoDB select the shard key?**

**Answer:**
Choosing the correct shard key is crucial for performance. The shard key determines how data is distributed across the shards. It should be chosen based on the following criteria:
- High cardinality (many unique values).
- Even distribution of data across shards.
- Frequently queried fields.

**Example:**
```js
db.orders.createIndex({ customer_id: 1 });
db.orders.shardCollection("orders", { customer_id: 1 });
```
In this example, the `customer_id` field is chosen as the shard key.

---

### 26. **MongoDB Indexing**

**Q71. What is the role of an index in MongoDB, and how does it improve query performance?**

**Answer:**
An index in MongoDB is a data structure that improves the speed of read operations by allowing MongoDB to quickly locate documents that match a query. Indexes are particularly useful for queries with filter conditions and sorting.

---

**Q72. How do you create a compound index in MongoDB?**

**Answer:**
A compound index is an index on multiple fields. It can improve query performance when filtering or sorting by multiple fields.

**Example:**
```js
db.users.createIndex({ age: 1, name: 1 });
```
This creates an index on both `age` and `name`, which improves performance for queries filtering or sorting by both fields.

---

**Q73. What is a geospatial index, and when would you use it?**

**Answer:**
A **geospatial index** is used for spatial queries, such as finding documents within a specific distance of a point or within a polygon. It is useful for location-based searches.

**Example:**
```js
db.places.createIndex({ location: "2dsphere" });

db.places.find({
  location: {
    $near: {
      type: "Point",
      coordinates: [40.7128, -74.0060]
    }
  }
});
```
This query finds places near the specified coordinates (New York City).

---

**Q74. What is the difference between a hashed index and a range index in MongoDB?**

**Answer:**
- **Hashed Index**: It indexes the hash of a field value, which is useful for evenly distributing data across shards when using sharding. It works well for equality queries.
- **Range Index**: It indexes the values directly and is useful for range-based queries (e.g., `>`, `<`, `>=`, `<=`).

**Example (Hashed Index):**
```js
db.users.createIndex({ username: "hashed" });
```

---

### 27. **Aggregation Framework**

**Q75. What is the purpose of the `$project` stage in MongoDB's aggregation pipeline?**

**Answer:**
The `$project` stage is used to reshape documents, allowing you to include or exclude fields, add computed fields, or rename fields. It modifies the output of the aggregation.

**Example:**
```js
db.users.aggregate([
  { $project: { name: 1, age: 1, isAdult: { $gte: ["$age", 18] } } }
]);
```
This projection adds an `isAdult` field based on the `age` field.

---

**Q76. What is the `$group` stage in MongoDB's aggregation pipeline, and how is it used?**

**Answer:**
The `$group` stage is used to group documents by a specified identifier and perform aggregation operations (e.g., `sum`, `average`, `count`) on grouped data.

**Example:**
```js
db.orders.aggregate([
  { $group: { _id: "$customer_id", totalAmount: { $sum: "$amount" } } }
]);
```
This groups orders by `customer_id` and calculates the total amount spent by each customer.

---

**Q77. What is the `$match` stage in MongoDB's aggregation pipeline, and how is it used?**

**Answer:**
The `$match` stage is used to filter documents based on specified conditions. It is similar to the `find()` query but used within an aggregation pipeline.

**Example:**
```js
db.orders.aggregate([
  { $match: { status: "completed" } },
  { $group: { _id: "$customer_id", totalAmount: { $sum: "$amount" } } }
]);
```
This filters orders with `status: "completed"` before grouping and calculating the total amount spent by each customer.

---

**Q78. How do you perform a join operation in MongoDB?**

**Answer:**
MongoDB provides the `$lookup` stage in the aggregation pipeline for performing left outer joins between collections. It combines documents from two collections based on a shared field.

**Example:**
```js
db.orders.aggregate([
  {
    $lookup: {
      from: "customers",
      localField: "customer_id",
      foreignField: "_id",
      as: "customer_details"
    }
  }
]);
```
This performs a left outer join between `orders` and `customers` based on the `customer_id` field.

---

### 28. **Backup and Recovery**

**Q79. How do you create a backup of a MongoDB database?**

**Answer:**
You can create a backup of a MongoDB database using the `mongodump` tool. This tool creates a binary dump of the database, which can later be restored using `mongorestore`.

**Example:**
```bash
mongodump --db mydb --out /backup/directory
```

---

**Q80. How do you restore a MongoDB database from a backup?**

**Answer:**
You can restore a MongoDB database using the `mongorestore` tool. It restores data from a backup created by `mongodump`.

**Example:**
```bash
mongorestore --db mydb /backup/directory/mydb
```

---

### 29. **Security**

**Q81. How does MongoDB handle authentication and authorization?**

**Answer:**
MongoDB provides authentication and authorization mechanisms to control access to databases and collections:
- **Authentication**: Verifies the identity of users (e.g., using username and password).
- **Authorization**: Determines the actions a user is allowed to perform based on roles.

You can enable authentication by setting up users with specific roles (e.g., `readWrite`, `dbAdmin`, etc.).

---

**Q82. How can you enable authentication in MongoDB?**

**Answer:**
To enable authentication in MongoDB, you need to start MongoDB with the `--auth` option and create a user with the required roles.

**Example:**
```bash
mongod --auth --bind_ip_all
```

Then, create a user with appropriate roles:
```js
db.createUser({
  user: "admin",
  pwd: "password",
  roles: [{ role: "root", db: "admin" }]
});
```

---

### 30. **Miscellaneous**

**Q83. How do you handle versioning in MongoDB?**

**Answer:**
MongoDB doesn't natively support versioning of documents, but you can implement versioning in your application by adding a `version` field to your documents. You can also use **timestamps** or **change streams** to track changes over time.

**Example:**
```js
db.users.updateOne(
  { _id: ObjectId("some_id") },
  { $set: { name: "John", version: 2 } }
);
```

---

**Q84. What is the `db.fsyncLock()` method used for?**

**Answer:**
The `db.fsyncLock()` method forces MongoDB to flush all in-memory data to disk. It is useful for taking a consistent backup of the database.

**Example:**
```js
db.fsyncLock();
```

To unlock it, use:
```js
db.fsyncUnlock();
```

---
Here are more MongoDB interview questions, answers, and examples:

### 31. **Replication and Fault Tolerance**

**Q85. What happens when the primary node in a replica set goes down?**

**Answer:**
When the primary node in a replica set goes down, MongoDB automatically triggers an election process to select a new primary from the secondaries. This ensures that the database remains available with minimal downtime.

- If the replica set has an **arbiter**, it helps in the election process.
- If the replica set doesn't have enough secondaries or if the remaining secondaries are not eligible to become the primary (due to factors like network partitioning), the replica set may become read-only until a new primary is elected.

---

**Q86. How does MongoDB handle read preferences in a replica set?**

**Answer:**
MongoDB allows you to configure **read preferences** to control where read operations are directed in a replica set. The following read preferences are available:
- **primary**: Reads are directed to the primary node.
- **primaryPreferred**: Reads are directed to the primary, but if it is unavailable, reads are directed to a secondary.
- **secondary**: Reads are directed to a secondary node.
- **secondaryPreferred**: Reads are directed to a secondary if possible; otherwise, they go to the primary.
- **nearest**: Reads are directed to the node with the least latency.

**Example:**
```js
db.getMongo().setReadPref('secondaryPreferred');
db.users.find();
```

---

**Q87. What is the role of the **`oplog`** in MongoDB replication?**

**Answer:**
The **`oplog`** (operations log) is a special capped collection in the primary node that records all write operations on the database. This log is then replicated to the secondary nodes in the replica set. The secondary nodes use the oplog to keep their data synchronized with the primary.

---

### 32. **Sharding**

**Q88. How does MongoDB distribute data in a sharded cluster?**

**Answer:**
MongoDB uses a **shard key** to determine how data is distributed across different shards in a sharded cluster. The shard key is chosen when a collection is sharded and is used to partition the data. Each shard holds a subset of the data, and MongoDB uses a **Mongos router** to direct queries to the correct shard.

**Example:**
```js
db.orders.createIndex({ customer_id: 1 });
db.orders.shardCollection("orders", { customer_id: 1 });
```
This would distribute data in the `orders` collection based on the `customer_id` field.

---

**Q89. What is a **mongos** in MongoDB sharding?**

**Answer:**
**Mongos** is a routing service that directs client requests to the appropriate shard in a sharded cluster. When you connect to a MongoDB sharded cluster, the client communicates with **mongos**, which then routes queries to the correct shard based on the shard key.

---

**Q90. How do you monitor the performance of a sharded cluster in MongoDB?**

**Answer:**
You can monitor the performance of a sharded cluster using:
- **MongoDB Atlas** for cloud-based monitoring.
- The **`sh.status()`** command to get a status of the sharded cluster, including shard distribution and chunk sizes.
- The **`db.currentOp()`** command to see the currently running operations.

```js
sh.status();  // Check the shard status
db.currentOp();  // Check active operations
```

---

### 33. **Data Modeling and Schema Design**

**Q91. What are the best practices for schema design in MongoDB?**

**Answer:**
Some best practices for schema design in MongoDB include:
1. **Embed data when it’s frequently accessed together**: For example, embed an array of comments within a blog post document.
2. **Reference data when relationships are many-to-many**: For example, store only references (ObjectIds) to users in an order document instead of embedding full user details.
3. **Consider read/write patterns**: If an application frequently updates a specific field, it’s better to index that field or store it in a way that minimizes updates.
4. **Design with scalability in mind**: Choose shard keys and indexes that will distribute data evenly across shards.

**Example of embedding:**
```js
db.posts.insertOne({
  title: "MongoDB Basics",
  author: "John",
  comments: [
    { user: "Alice", comment: "Great post!" },
    { user: "Bob", comment: "Very helpful!" }
  ]
});
```

**Example of referencing:**
```js
db.orders.insertOne({
  orderId: "12345",
  userId: ObjectId("someUserId"),
  productIds: [ObjectId("productId1"), ObjectId("productId2")]
});
```

---

**Q92. What is the difference between embedding and referencing in MongoDB schema design?**

**Answer:**
- **Embedding**: Store related data within a document. Best for data that is frequently accessed together and does not grow unbounded.
- **Referencing**: Store references (ObjectIds) to related data in separate documents. Best for data that grows unbounded, such as user profiles or products in a catalog.

---

**Q93. How would you model a one-to-many relationship in MongoDB?**

**Answer:**
In a one-to-many relationship, you could either embed the "many" documents inside the "one" document (if the number of "many" documents is small and unlikely to grow unbounded) or reference them by storing the ObjectIds of the "many" documents.

**Example (embedding):**
```js
db.author.insertOne({
  name: "J.K. Rowling",
  books: [
    { title: "Harry Potter and the Sorcerer's Stone", year: 1997 },
    { title: "Harry Potter and the Chamber of Secrets", year: 1998 }
  ]
});
```

**Example (referencing):**
```js
db.authors.insertOne({ name: "J.K. Rowling" });
db.books.insertMany([
  { title: "Harry Potter and the Sorcerer's Stone", authorId: ObjectId("authorId1") },
  { title: "Harry Potter and the Chamber of Secrets", authorId: ObjectId("authorId1") }
]);
```

---

### 34. **Aggregation and Pipeline**

**Q94. What is the `$facet` stage in MongoDB’s aggregation pipeline?**

**Answer:**
The `$facet` stage allows you to perform multiple aggregation pipelines within a single stage. It’s useful for scenarios where you need to perform different kinds of aggregations simultaneously and return the results together in one document.

**Example:**
```js
db.orders.aggregate([
  {
    $facet: {
      "byStatus": [{ $group: { _id: "$status", count: { $sum: 1 } } }],
      "byDate": [{ $group: { _id: { $month: "$orderDate" }, totalAmount: { $sum: "$amount" } } }]
    }
  }
]);
```
This performs two separate aggregations: one grouping by order status and another by month.

---

**Q95. What is the `$unwind` stage in MongoDB’s aggregation pipeline?**

**Answer:**
The `$unwind` stage deconstructs an array field from the input documents to output a document for each element in the array. This is useful for performing aggregations or queries on array elements.

**Example:**
```js
db.orders.aggregate([
  { $unwind: "$items" },
  { $group: { _id: "$items.productId", totalQuantity: { $sum: "$items.quantity" } } }
]);
```
This unwinds the `items` array and groups by `productId` to calculate the total quantity for each product.

---

### 35. **Backup and Disaster Recovery**

**Q96. How do you take a backup of a sharded MongoDB cluster?**

**Answer:**
Taking a backup of a sharded MongoDB cluster requires using `mongodump` on each shard and the config server. Alternatively, you can use **MongoDB Atlas** for automated backups.

To back up from all shards:
```bash
mongodump --host <shard1_host> --port <shard1_port> --out /backup/directory
mongodump --host <shard2_host> --port <shard2_port> --out /backup/directory
```

Additionally, use `mongorestore` to restore:
```bash
mongorestore --host <shard1_host> --port <shard1_port> /backup/directory
```

---

**Q97. What is the role of `db.copyDatabase()` in MongoDB?**

**Answer:**
The `db.copyDatabase()` command is used to copy a database from one MongoDB server to another. It is often used for backup or migration purposes.

**Example:**
```js
db.copyDatabase("mydb", "mydb_copy", "source_host", "source_port");
```

---

### 36. **Security and Authentication**

**Q98. How can you enable Role-Based Access Control (RBAC) in MongoDB?**

**Answer:**
To enable Role-Based Access Control (RBAC), MongoDB must be started with authentication enabled. You can then create users and assign roles with specific privileges.

**Example:**
```bash
mongod --auth --bind_ip_all
```

To create a user with a role:
```js
db.createUser({
  user: "readOnlyUser",
  pwd: "password123",
  roles: [{ role: "read", db: "mydb" }]
});
```

---

**Q99. How does MongoDB handle encryption at rest?**

**Answer:**
MongoDB supports **encryption at rest** by using the **WiredTiger storage engine** with encryption enabled. Encryption can be configured by specifying the encryption key during the database startup.

**Example (configuring encryption):**
```yaml
security:
  enableEncryption: true
  encryptionKeyFile: /path/to/keyfile
```

---

**Q100. What is the **`$redact`** stage in MongoDB’s aggregation pipeline?**

**Answer:**
The `$redact` stage is used to control access to specific fields or documents based on their values. It allows you to redact (hide) parts of the document that match certain conditions.

**Example:**
```js
db.orders.aggregate([
  {
    $redact: {
      $cond: {
        if: { $eq: ["$status", "completed"] },
        then: "$$KEEP",
        else: "$$PRUNE"
      }
    }
  }
]);
```
This removes documents where the `status` is not `"completed"`.

---
