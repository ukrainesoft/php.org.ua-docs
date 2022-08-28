Встановлює максимальний період кандидата

-   [« fann\_set\_cascade\_candidate\_stagnation\_epochs](function.fann-set-cascade-candidate-stagnation-epochs.html)
    
-   [fann\_set\_cascade\_max\_out\_epochs »](function.fann-set-cascade-max-out-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює максимальний період кандидата
    

# fannsetcascademaxcandepochs

(PECL fann> = 1.0.0)

fannsetcascademaxcandepochs - Встановлює найбільший період кандидата

### Опис

```methodsynopsis
fann_set_cascade_max_cand_epochs(resource $ann, int $cascade_max_cand_epochs): bool
```

Встановлює максимальний період кандидата.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_max_cand_epochs`

Максимальний період кандидата.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_max\_cand\_epochs()](function.fann-get-cascade-max-cand-epochs.html) - Отримує найбільший період кандидата