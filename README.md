# Mock_SQL

## Please submit the interview problems posted in slack channel here. The problems and statements are intentionally not shown here so that students are not able to see them in advance 
### Write your MySQL query statement below
SELECT u.name, ifnull(sum(r.distance),0) as travelled_distance
from Users u left join rides r on u.id=r.user_id 
group by u.id
order by travelled_distance desc, u.name

### Write your MySQL query statement below
SELECT sale_date, sum(case when fruit='apples' then sold_num else -sold_num end) as diff
from sales
group by sale_date
