# Database
1. Check database perfromance
A. Using external tools

2. Find Duplicates of employee name in table of employee
A. select name from employee
   group by name
   having count(*) > 1

