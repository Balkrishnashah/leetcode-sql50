## Question

https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/?envType=study-plan-v2&envId=top-sql-50

## Solution

```sql
# Write your MySQL query statement below 
select 
customer_id,
count(a.visit_id) as count_no_trans
from Visits a left join
Transactions b
on a.visit_id = b.visit_id 
where transaction_id is null
group by customer_id
