# DB-UNIVERSITY

## 1. Selezionare tutti gli studenti nati nel 1990 (160)

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

## 2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

```SQL
SELECT *
FROM `courses`
WHERE `cfu` > 10;
```

## 3. Selezionare tutti gli studenti che hanno più di 30 anni

```SQL
SELECT date_of_birth, name, YEAR(current_date()) - YEAR(`date_of_birth`) AS age
FROM `students`
WHERE YEAR(current_date()) - YEAR(`date_of_birth`) > 30;

SELECT *
FROM `students`
WHERE 2024 - YEAR(`date_of_birth`) > 30;
```

## 4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)

```SQL
SELECT *
FROM `courses`
WHERE `period` = 'I semestre' AND `year` = 1;
```

## 5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)

```SQL
SELECT *
FROM `exams`
WHERE TIME(`hour`) > '14:00:00' AND `date` = '2020-06-20';
```

## 6. Selezionare tutti i corsi di laurea magistrale (38)

```SQL
SELECT *
FROM `degrees`
WHERE `level` = 'magistrale';

SELECT *
FROM `degrees`
WHERE `name` LIKE '%magistrale%';
```

## 7. Da quanti dipartimenti è composta l'università? (12)

```SQL
SELECT *
FROM `departments`;

SELECT count(*) AS 'number_of_departments'
FROM `departments`;
```

## 8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

```SQL
SELECT *
FROM `teachers`
WHERE `phone` IS NOT NULL;
```

## 9. inserire nella tabella degli studenti un nuovo record con i propri dati (per il campo degree_id, inserire un valore casuale)

## 10. Cambiare il numero dell'ufficio del professore Pietro Rizzo in 126

## 11. Eliminare dalla tabella studenti il record creato precedentemente al punto 9
