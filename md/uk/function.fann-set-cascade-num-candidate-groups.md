Встановлює кількість груп кандидатів

-   [« fann\_set\_cascade\_min\_out\_epochs](function.fann-set-cascade-min-out-epochs.html)
    
-   [fann\_set\_cascade\_output\_change\_fraction »](function.fann-set-cascade-output-change-fraction.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює кількість груп кандидатів
    

# fannsetcascadenumcandidategroups

(PECL fann> = 1.0.0)

fannsetcascadenumcandidategroups - Встановлює кількість груп кандидатів

### Опис

```methodsynopsis
fann_set_cascade_num_candidate_groups(resource $ann, int $cascade_num_candidate_groups): bool
```

Встановлює кількість груп кандидатів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_num_candidate_groups`

Кількість груп кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_num\_candidate\_groups()](function.fann-get-cascade-num-candidate-groups.html) - Повертає кількість груп кандидатів