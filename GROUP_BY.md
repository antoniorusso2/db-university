# DB-UNIVERSITY

## 1. Contare quanti iscritti ci sono stati ogni anno

```SQL
SELECT COUNT(*) AS `count`, YEAR(`enrolment_date`) AS `year`
FROM `students`
GROUP BY YEAR(`enrolment_date`);
```

## 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```SQL
SELECT `office_address`, COUNT(*) AS `teachers_count`
FROM `teachers`
GROUP BY `office_address`;
```

## 3. Calcolare la media dei voti di ogni appello d'esame

```SQL
SELECT AVG(`vote`) AS `average`, `exam_id`
FROM `exam_student`
GROUP BY `exam_id`;
```

## 4. Contare quanti corsi di laurea ci sono per ogni dipartimento
