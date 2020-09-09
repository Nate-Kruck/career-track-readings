# Class 03 Readings (Sept. 8th)

## Inside a Computer

- Motherboard - The main curcuit board for the computer. It holds the CPU, GPU, memory and all the good stuff that makes your computer run.

- CPU/Processor - the central processing unit. This bad boy here the brain of the computer and its main job is to carry out commands. Everytime you interact with your computer you are sending the CPU instructions.

- RAM - random access memory, short term memory for the computer. RAM temporarily stores data until it is needed.

- Hard drive/SSD/NVME - the memory. Hard drives used to be the standard then the world started transitioning to SSD for faster read/write times and now we are moving towards NVME SSD. These are about 3-4 inches long and a few mm thick so they are tiny pieces of hardware, but they make the HDD and SSD cards look like turtles racing against cheetas.

- Power Supply Unit - converts the power from the wall outlet to the type of power needed by a computer. The higher the wattage the less chance you have to ruin your computer (depending on the type of hardware your computer is using)

  - Expansion cards

    - Video Cards

    - Sound Cards

    - Network Cards

---

## SQL INSERT

- INSERT allows you to insert a new row into a table

- If you want to return the entire inserted row, you use an asterisk (\*) after the RETURNING keyword:

```SQL
INSERT INTO table_name(column1, column2, …)
VALUES (value1, value2, …)
RETURNING *;
```

## SQL SELECT

- SELECT statement retrieves data from a single table.

- Syntax of the SELECT statement:

```SQL
SELECT
   select_list
FROM
   table_name;
```

## SQL UPDATE

- UPDATE - The PostgreSQL UPDATE statement allows you to modify data in a table.

- Syntax of the UPDATE statement:

```SQL
UPDATE table_name
SET column1 = value1,
    column2 = value2,
    ...
WHERE condition;
```

## SQL DELETE

- The PostgreSQL DELETE statement allows you to delete one or more rows from a table.

- Syntax of the DELETE statement:

```SQL
DELETE FROM table_name
WHERE condition;
```
