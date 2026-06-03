## Question

https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/description/?envType=study-plan-v2&envId=top-sql-50

## Solution

```sql
# Write your MySQL query statement below
select
a.unique_id ,
b.name
from EmployeeUNI a
right join Employees b 
on a.id = b.id 
