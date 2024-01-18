# Products Table Analysis

## Table Structure

Below is the structure of the `Products` table:

| Column Name | Type    |
|-------------|---------|
| product_id  | int     |
| low_fats    | enum    |
| recyclable  | enum    |

- `product_id` is the primary key for this table, meaning each value is unique.
- `low_fats` is an ENUM type with values ('Y', 'N'), where 'Y' indicates a low-fat product and 'N' indicates otherwise.
- `recyclable` is an ENUM type with values ('Y', 'N'), where 'Y' indicates the product is recyclable and 'N' indicates it is not.

## Objective

The goal is to find the IDs of products that are both low in fats and recyclable.

## Solution

To achieve this, we can perform a query that selects product IDs where both `low_fats` and `recyclable` columns have the value 'Y'.

## Example

### Input

Consider the following example of a `Products` table:

| product_id  | low_fats | recyclable |
|-------------|----------|------------|
| 0           | Y        | N          |
| 1           | Y        | Y          |
| 2           | N        | Y          |
| 3           | Y        | Y          |
| 4           | N        | N          |

### Output

The query should return:

| product_id  |
|-------------|
| 1           |
| 3           |

### Explanation

Only products 1 and 3 meet the criteria of being both low fat and recyclable.
