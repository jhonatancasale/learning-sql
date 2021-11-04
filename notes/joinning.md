General idea of inner join
--------------------------

```sql
select * from <left_table> inner join <right_table> on left_table.id = right_table.id
-- eventually, we can shorthand this by
select * from <left_table> inner join <right_table> using(id); -- or ...
select * from <left_table> as a inner join <right_table> as b using(id);
```
