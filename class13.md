# Class 13 Readings (Sept. 29th)

## Mongo Aggregations

- The aggregation pipeline is a framework for data on the concept of data processing pipelines.

- The MongoDB aggregation pipeline consists of stages. Each stage transforms the documents as they pass through the pipeline. 

### Pipeline Expressions

- Some pipeline stages a pipeline expression as the operand. Pipeline expressions specify the transformation to apply to the input documents. Expressions have a document structure and can contain other expression.

### Operators and Indexes

- $match - the $match stage can use an index to filter documents if it occurs at the beginning of a pipeline
- $sort - This stage can use an index as long as it is not preceded by a $project, $unwind, or $group stage
- $group - The $group stage can sometimes use an index to find the first document in each group if all of the following criteria are met:

The $group stage is preceded by a $sort stage that sorts the field to group by,
There is an index on the grouped field which matches the sort order and
The only accumulator used in the $group stage is $first.

- $geoNear - The $geoNear pipeline operator takes advantage of a geospatial index. When using $geoNear, the $geoNear pipeline operation must appear as the first stage in an aggregation pipeline.

### Early Filtering

- if aggregation operation requires only subset of the data in a collection, use ($match, $limit, $skip) stages to restrict the documents that enter at the beginning of the pipeline.

## Aggregations by Example

### Starting an Aggregation Pipeline

- Getting an aggregation pipeline started is a simple affair: simply call the aggregate function on any collection.

- The aggregate function accepts an array of data transformations which are applied to the data in the order they're defined.

### Matching Documents

- The first stage of the pipeline is matching, and that allows us to filter out documents so that we're only manipulating the documents we care about. The matching expression looks and acts much like the MongoDB find function or a SQL WHERE clause.