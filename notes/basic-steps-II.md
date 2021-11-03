Aggregate funcions
------------------
```sql
select avg(<field>) from <table>;
select max(<field>) from <table>;
select min(<field>) from <table>;
select sum(<field>) from <table>;
```

Basic arithmetic
----------------
```sql
select (4 * 3); -- +, -, *, /
select (4 / 3); -- => 1, because it is the integer division
select (4.0 / 3); -- => will produce the expected 1.333333...
```

Alias
-----
```sql
select max(<field>), max(<field_b>) from <table>; -- will produce max and max as table result field to avoid this ...
select max(<field>) as "Max field", max(<field_b>) as "Max field_b" from <table>;
```

Order by
--------
```sql
select <field> from <table> order by <field_b> [desc];
select <field_b>[, field]+ from <table> order by <field_b>[, field]+ -- the comumn order does matter
```

Group by
--------
```sql
select <field>, count(*) from <table> group by <field>; -- to count how much of <field> do we have
-- we NEED to SELECT the field that we're attempting to group by
select <field>, count(*) from <table> group by <field> order by count desc;
-- in a general query
select <field>[, <field_b>][, count(<field|wildcard>)] from <table>[group by <field>][order by <field>];
-- we can't sort values that we havent't calculated yet!
-- in SQL I cant [use](use) aggregate functions with WHERE, to proper filter the
-- result from the aggregate function, we need to use HAVING
select <field> from <table> group by <field> having count(field_b) > 10;
-- but I can do something like this
select <field>, avg(field_b) as B, avg(field_c) as C from <table> where field > 10 group by field having avg(field_b) > 100 order by C desc;
```
