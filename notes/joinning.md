General idea of inner join
--------------------------

```sql
select * from <left_table> inner join <right_table> on left_table.id = right_table.id
-- eventually, we can shorthand this by
select * from <left_table> inner join <right_table> using(id); -- or ...
select * from <left_table> as a inner join <right_table> as b using(id);
```
```sql
SELECT field[, field4]
    CASE WHEN field4 > 2000000 THEN 'A'
        WHEN field4 > 350000 THEN 'B'
        ELSE 'C' END
        AS field_group
FROM <table>;
```

