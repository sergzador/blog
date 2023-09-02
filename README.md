# Designing Data Warehouse

## Checklist

1. Design Principles:
   - data model
   - transformations
2. Naming Conventions
   -  List of abbreviations
   -  Objects
   -  Columns
   -  Keys
3. Conceptual Model
4. Logical & Physical Model
5. Transformational Model
6. Keys and IDs (consider short keys)
7. Data Types
   - timezones
   - MD5 binary vs varchar

## Data Model Design Principles

1. Efficient
2. Easy to understand
3. Mandatory table design properties (eg."is scd2")
4. If MD5 is used, full MD5 function with arguments should be documented at the table level
5. 100% Consistency

## Transformations Design Principles

1. Fixes of DQ issues in code, should not result in DQ issues downstream
2. Transformations should be built to enable complete model refresh (data)
3. Back up strategy alligning with Code change process.For example if all is managed via repo how do you do DB back up/recovery

## Naming Conventions
1. Objects:
   - Tables and Views should not be distinguished by the name (e.g. _V). This is because materialization might change in the future.
   - Singular for object names
   - entity names should not be included in the column name, unless it's a key column (e.g. customer_name)
2. Keys:

## Keys and IDs (consider short keys)
1. column name pattern for primary key columns (_key vs _id)
2. sequences vs identity vs MD5
3. 
