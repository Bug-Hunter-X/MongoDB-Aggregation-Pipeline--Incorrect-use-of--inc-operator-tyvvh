# MongoDB Aggregation Pipeline Bug: Incorrect $inc Operator Usage

This repository demonstrates a common error when using the `$inc` operator within a MongoDB aggregation pipeline.  The issue arises from applying `$inc` after a `$limit` stage, impacting all documents instead of the intended subset.

## Bug Description
The provided JavaScript code snippet showcases an aggregation pipeline that aims to find the top 10 most frequent items. However, due to the incorrect placement of `$inc`, the counts for all documents are incremented, altering the final result.

## Bug Solution
The solution involves restructuring the aggregation pipeline to correctly apply `$inc` before the `$limit` stage, ensuring that the increment operation only affects the intended documents.
