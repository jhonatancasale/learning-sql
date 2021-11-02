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
select <from> from <table> order by <field_b> [desc];
```` 
