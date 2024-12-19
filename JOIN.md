# DB-UNIVERSITY

## 1. Selezionare tutti gli studenti iscritti al corso di Laurea in Economia

```SQL
SELECT `students`.`name` AS `student_name`, `degrees`.`name` AS `degree`
FROM `students`
JOIN `degrees`
ON `degrees`.`id` = `students`.`degree_id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

SELECT `students`.`name` AS `student_name`, `degrees`.`name` AS `degree`
FROM `students`
JOIN `degrees`
ON `degrees`.`id` = `students`.`degree_id`
WHERE `degrees`.`name` LIKE "%economia%";
```

## 2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

```SQL
SELECT `degrees`.`name` AS `degree`, `degrees`.`level` AS `level` , `departments`.`name` AS `department`
FROM `degrees`
JOIN `departments`
ON `departments`.`id` = `degrees`.`department_id`
WHERE `degrees`.`level` = 'magistrale' AND `degrees`.`department_id` = 7;
```

## 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

## 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

## 5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

## 6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

## 7. BONUS: Selezionare per ogni studente iil numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con il voto minimo 18
