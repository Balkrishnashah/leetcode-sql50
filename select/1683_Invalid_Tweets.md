## Question

https://leetcode.com/problems/invalid-tweets/description/?envType=study-plan-v2&envId=top-sql-50

## Solution

```sql
# Write your MySQL query statement below
select tweet_id
from Tweets
where length(content) > 15