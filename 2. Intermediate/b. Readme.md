### Operators in MongoDB





1. Query Operators
Used to specify criteria for selecting documents.

- $eq: Matches values that are equal to a specified value.
- $ne: Matches values that are not equal to a specified value.
- $gt: Matches values that are greater than a specified value.
- $gte: Matches values that are greater than or equal to a specified value.
- $lt: Matches values that are less than a specified value.
- $lte: Matches values that are less than or equal to a specified value.
- $in: Matches values that are in a specified array.
- $nin: Matches values that are not in a specified array.




2. Update Operators
Used to modify documents in an update operation.

$set: Sets the value of a field.
$unset: Removes a field.
$inc: Increments the value of a field by a specified amount.
$push: Adds an item to an array.





3. Aggregation Operators
Used in the aggregation framework to process and transform data.

$sum: Calculates the sum of values.
$avg: Calculates the average of values.
$max: Finds the maximum value.
$min: Finds the minimum value.
$group: Groups documents together and performs aggregate operations.
$project: Reshapes documents by adding or removing fields.







4. Array Operators
Used to work with arrays in queries and updates.

$elemMatch: Matches documents that contain an array field with at least one element that matches all the specified query criteria.
$size: Matches arrays with a specified number of elements.






5. Projection Operators
Used to specify or exclude fields in the result set.

$slice: Limits the number of elements in an array field returned in the query result.





