# MongoDB $inc operator error with incorrect value type
This repository demonstrates a common error when using the `$inc` operator in MongoDB update operations. The error occurs when providing a non-numeric value to the `$inc` operator, leading to unexpected behavior or an error.

## Bug Description
The `$inc` operator is used to increment or decrement a numeric field. If a non-numeric value is passed, MongoDB cannot perform the increment operation, resulting in an error. This bug showcases this issue and its solution.

## Bug Reproduction
1. Clone the repository.
2. Create a MongoDB collection named `myCollection`.
3. Insert a document with the `_id` as `ObjectId("someId")` (replace with a valid ObjectId). 
4. Run the `bug.js` script which will attempt to increment a field using a non-numeric value and an error will be thrown.

## Solution
The `bugSolution.js` demonstrates the correct usage of the `$inc` operator by ensuring a numeric value is provided.
