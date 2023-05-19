## Comandos SQLite más usados

### Crear una tabla

```sql

CREATE TABLE table_name (
    column1 datatype PRIMARY KEY,
    column2 datatype NOT NULL,
    column3 datatype DEFAULT value,
    ...
);

```

### Insertar datos

```sql

INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

```

### Consultar Datos 

```sql

SELECT column1, column2, ...
FROM table_name
WHERE condition
ORDER BY column ASC|DESC
LIMIT number;

```

### Actualizar datos

```sql

UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

```

### Eliminar datos

```sql

DELETE FROM table_name
WHERE condition;

```

### Crear un índice 

```sql

CREATE INDEX index_name
ON table_name (column_name);

```

### Eliminar un índice 

```sql

DROP INDEX index_name;

```

### Eliminar una tabla 

```sql

DROP TABLE table_name;

```

### Realizar una unión entre tablas (JOIN)

```sql

SELECT column1, column2, ...
FROM table1
JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;

```

### Agrupar datos (GROUP BY)

```sql

SELECT column1, COUNT(*)
FROM table_name
GROUP BY column1
HAVING condition;

```

### Crear una vista

```sql

CREATE VIEW view_name AS
SELECT column1, column2, ...
FROM table_name
WHERE condition;

```

### Eliminar una vista

```sql

DROP VIEW view_name;

```

### Realizar una transacción 

```sql

BEGIN TRANSACTION;
-- SQL statements
COMMIT;
-- or
ROLLBACK;

```

[Documentación oficial](https://sqlite.org/docs.html)

[Volver](/SQL.md)
