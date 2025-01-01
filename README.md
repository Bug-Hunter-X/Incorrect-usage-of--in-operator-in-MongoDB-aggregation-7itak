# Incorrect usage of $in operator in MongoDB aggregation
This repository contains a demonstration of an incorrect usage of the $in operator in MongoDB aggregation pipelines.
The incorrect usage leads to unexpected results. The correct usage is also provided for comparison.  The issue arises when attempting to filter documents based on multiple values using $in and simultaneously selecting specific fields for projection.

## Bug
The bug lies in the incorrect placement of the projection within the MongoDB query using the $in operator.  The original code attempted to filter and project within the find() method, causing the unexpected behavior.

## Solution
The solution correctly uses the find() method for filtering using $in and then chain a separate project() method to select the required fields.

## How to reproduce the bug
1.  Clone this repository.
2.  Run the `bug.js` file. This will demonstrate the incorrect usage.
3.  Run the `bugSolution.js` file. This demonstrates the corrected version.
