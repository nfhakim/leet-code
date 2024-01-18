# Customer Referral Analysis

## Table Structure

The structure of the `Customer` table is as follows:

| Column Name | Type    |
|-------------|---------|
| id          | int     |
| name        | varchar |
| referee_id  | int     |

- `id` is the primary key of the table, representing the unique identifier for each customer.
- `name` is a varchar type, indicating the name of the customer.
- `referee_id` is an int type, representing the ID of the customer who referred them.

## Objective

The goal is to find the names of customers who were not referred by the customer with `id = 2`.

## Approach

We need to select customer names from the table where the `referee_id` is not 2. This includes customers with `referee_id` as NULL or any other value except 2.

## Example

### Input

Consider the following `Customer` table as an example:

| id | name | referee_id |
|----|------|------------|
| 1  | Will | null       |
| 2  | Jane | null       |
| 3  | Alex | 2          |
| 4  | Bill | null       |
| 5  | Zack | 1          |
| 6  | Mark | 2          |

### Output

The query should result in the following output:

| name |
|------|
| Will |
| Jane |
| Bill |
| Zack |

### Explanation

The names listed (Will, Jane, Bill, Zack) are those of customers who were not referred by the customer with `id = 2`.
