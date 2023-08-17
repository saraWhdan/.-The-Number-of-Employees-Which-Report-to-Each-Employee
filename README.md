# -The-Number-of-Employees-Which-Report-to-Each-Employee

Problem Link: https://leetcode.com/problems/the-number-of-employees-which-report-to-each-employee/description/?envType=study-plan-v2&envId=top-sql-50

## Solution

```sql
select m.employee_id
,m.name 
,count(e.employee_id) reports_count
,ROUND(avg(e.age*  1.0),0) average_age from Employees m
inner join Employees e on m.Employee_id=e.reports_to
group by m.employee_id,m.name 
order by m.employee_id
```
