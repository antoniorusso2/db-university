# DB-UNIVERSITY

## Selezionare tutti gli studenti nati nel 1990 (160)

```SQL
SELECT *
FROM `students`
WHERE YEAR(`date_of_birth`) = 1990;

SELECT *
FROM `students`
WHERE `date_of_birth` LIKE '1990-%';

SELECT *
FROM `students`
WHERE `date_of_birth` BETWEEN '1990-01-01' AND '1990-12-31';
```
