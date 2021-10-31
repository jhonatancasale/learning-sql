Fields or (features) are the same  as Columns

Register or entry means Rows


Basic Steps
===========

Generic select idea
-------------------

```sql
select <field> from <table>;
select <field>[, field]* from <table>;
select count(*) from <table>;
select count(field) from <table>;
select count(distinct field) from <table>;
```

Relational operators
--------------------

```sql
=  -- equal
<> -- not equal; SQL standard mean <> and not !=
<  -- less than
>  -- greater than
<= -- less than or equal to
>= -- greater than or equal to
```

Examples
--------
```sql
select <field> from <table> where <field> = 'criteria'; -- single quotes (') could be different among the databases
select <field> from <table> where <numeric_field> > criteria;
```

Logical operators
-----------------

```sql
-- AND
select <field> from <table> where CONDITION AND CONDITION;
select <field> from <table> where CONDITION_A AND CONDITION_B AND CONDITION_C;

-- OR
select <field> from <table> where CONDITION OR CONDITION;
select <field> from <table> where CONDITION_A OR CONDITION_B OR CONDITION_C;

-- BETWEEN
select <field> from <table> where <field_a> >= 100 AND <field_a> <= 200;
-- is the same as
select <field> from <table> where field_a BETWEEN 100 AND 200;
-- therefore, BETWEEN is _inclusive_

-- IN
select <field> from <table> where <field_b> in (1, 3, 5, 6, 7);

```
