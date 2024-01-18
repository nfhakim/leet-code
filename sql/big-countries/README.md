# Analysis of Big Countries

## Table Structure

The `World` table is structured as follows:

| Column Name | Type    |
|-------------|---------|
| name        | varchar |
| continent   | varchar |
| area        | int     |
| population  | int     |
| gdp         | bigint  |

- `name` is the primary key of this table and it represents the unique name of a country.
- The table includes information about each country's continent, area (in km²), population, and GDP value.

## Objective

The task is to find the name, population, and area of countries classified as "big". A country is considered big if:
- It has an area of at least three million km² (i.e., 3000000 km²), or
- It has a population of at least twenty-five million (i.e., 25000000).

## Approach

To determine the big countries, we'll select the `name`, `population`, and `area` of countries from the table where either the `area` is ≥ 3000000 km² or the `population` is ≥ 25000000.

## Example

### Input

Consider the following example of a `World` table:

| name        | continent | area    | population | gdp          |
|-------------|-----------|---------|------------|--------------|
| Afghanistan | Asia      | 652230  | 25500100   | 20343000000  |
| Albania     | Europe    | 28748   | 2831741    | 12960000000  |
| Algeria     | Africa    | 2381741 | 37100000   | 188681000000 |
| Andorra     | Europe    | 468     | 78115      | 3712000000   |
| Angola      | Africa    | 1246700 | 20609294   | 100990000000 |

### Output

The expected output would be:

| name        | population | area    |
|-------------|------------|---------|
| Afghanistan | 25500100   | 652230  |
| Algeria     | 37100000   | 2381741 |

### Explanation

In this example, Afghanistan and Algeria are considered big countries because Afghanistan has a population greater than 25 million and Algeria has both a significant population and a large area.
