---
layout: article
title: mybro
tags: TeXt
---

If you see this page, that means you have setup your site. enjoy! :ghost: :ghost: :ghost:



```sql

SELECT YEAR(SYSDATE())
FROM   hr_employees

SELECT concat(first_name,' ',last_name),date_format(SYSDATE(),'%Y') - date_format(HIRE_DATE,'%Y') AS '재직기간'
FROM   hr_employees


SELECT employee_id, timestampdiff(year,hire_date,SYSDATE()) AS 재직기간
FROM   hr_employees

SELECT employee_id, round(DATEDIFF(SYSDATE(), hire_date)/365,0)
FROM   hr_employees

SELECT *
FROM   hr_employees

```
