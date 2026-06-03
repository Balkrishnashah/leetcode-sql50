## Question

https://leetcode.com/problems/product-sales-analysis-i/?envType=study-plan-v2&envId=top-sql-50

## Solution

```sql
# Write your MySQL query statement below
select 
product_name,
year,
price 
from (
    select sale_id, product_name,year,sum(price) as price
    from Sales inner join Product
    on Sales.product_id = Product.product_id
      group by 1,2,3 
) abc
