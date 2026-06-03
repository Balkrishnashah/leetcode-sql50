## Question

[\[Click To Open Question on LeetCode\]](https://leetcode.com/problems/average-time-of-process-per-machine/?envType=study-plan-v2&envId=top-sql-50)

## Solution

```sql
# Write your MySQL query statement below
select
a.machine_id,
round(sum(b.timestamp - a.timestamp)/count(a.process_id),3) as processing_time
from Activity a inner join Activity b
on a.machine_id = b.machine_id and a.process_id = b.process_id
where a.activity_type = 'start' and b.activity_type = 'end'
group by 1