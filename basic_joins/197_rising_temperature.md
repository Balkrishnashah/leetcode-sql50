## Question

https://leetcode.com/problems/rising-temperature/?envType=study-plan-v2&envId=top-sql-50

## Solution

```sql
# Write your MySQL query statement below
select a.id
from Weather a inner join Weather b
on a.recordDate = date_add(b.recordDate, INTERVAL 1 DAY)
and a.temperature > b.temperature