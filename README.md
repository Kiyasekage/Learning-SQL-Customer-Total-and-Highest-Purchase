# Customer Total and Highest Purchase

This project is a SQL practice exercise that demonstrates the use of aggregate functions with `GROUP BY`. The query groups orders by `customer_id` and calculates the total amount spent by each customer using `SUM()`, while also finding the highest individual purchase made by each customer using `MAX()`. This project helps practice analyzing customer purchase data and working with aggregate functions in SQL.

## SQL Query

```sql
SELECT customer_id,
       SUM(total_amount),
       MAX(total_amount) AS highest_purchase
FROM orders
GROUP BY customer_id;
```

## Concepts Practiced

* `SELECT`
* `SUM()`
* `MAX()`
* `GROUP BY`
* Column aliases using `AS`
* Aggregate functions
* Grouping data by customer

## What the Query Does

* **`customer_id`** → Identifies each customer.
* **`SUM(total_amount)`** → Calculates the total amount spent across all orders made by each customer.
* **`MAX(total_amount)`** → Finds the highest individual order amount for each customer.
* **`GROUP BY customer_id`** → Groups all orders belonging to the same customer so the aggregate calculations are performed separately for each customer.

## Example Output

```text
+-------------+-------------------+-----------------+
| customer_id | SUM(total_amount) | highest_purchase|
+-------------+-------------------+-----------------+
|      1      |        450000      |      250000     |
|      2      |        780000      |      400000     |
|      3      |        320000      |      180000     |
+-------------+-------------------+-----------------+
```

## Language

* SQL
* MySQL
