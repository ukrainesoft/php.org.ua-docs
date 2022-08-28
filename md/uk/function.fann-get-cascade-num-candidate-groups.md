Повертає кількість груп кандидатів

-   [« fann\_get\_cascade\_min\_out\_epochs](function.fann-get-cascade-min-out-epochs.html)
    
-   [fann\_get\_cascade\_num\_candidates »](function.fann-get-cascade-num-candidates.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає кількість груп кандидатів
    

# fanngetcascadenumcandidategroups

(PECL fann> = 1.0.0)

fanngetcascadenumcandidategroups — Повертає кількість груп кандидатів

### Опис

```methodsynopsis
fann_get_cascade_num_candidate_groups(resource $ann): int
```

Кількість груп кандидатів – це кількість груп однакових кандидатів, які використовуватимуться під час навчання.

Кількість можна використовувати, щоб збільшити кількість кандидатів без необхідності визначати нові параметри для кандидатів.

Дивіться [fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.html) для опису того, які нейрони-кандидати будуть згенеровані цим параметром.

Кількість груп кандидатів за умовчанням дорівнює 2.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість груп кандидатів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_cascade\_num\_candidate\_groups()](function.fann-set-cascade-num-candidate-groups.html) - встановлює кількість груп кандидатів