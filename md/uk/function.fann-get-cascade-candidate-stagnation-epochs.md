Повертає кількість періодів застою каскаду кандидата

-   [« fann\_get\_cascade\_candidate\_limit](function.fann-get-cascade-candidate-limit.html)
    
-   [fann\_get\_cascade\_max\_cand\_epochs »](function.fann-get-cascade-max-cand-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає кількість періодів застою каскаду кандидата
    

# fanngetcascadecandidatestagnationepochs

(PECL fann> = 1.0.0)

fanngetcascadecandidatestagnationepochs - Повертає кількість періодів застою каскаду кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_stagnation_epochs(resource $ann): int
```

Кількість періодів застою каскаду кандидата визначає кількість періодів, яким дозволено продовжити навчання без зміни MSE на частку [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.html)

Дивіться додаткову інформацію про цей параметр у [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.html)

За замовчуванням кількість періодів застою каскаду кандидата дорівнює 12.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість періодів застою каскаду кандидата або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_cascade\_candidate\_stagnation\_epochs()](function.fann-set-cascade-candidate-stagnation-epochs.html) - встановлює кількість каскадних періодів застою кандидатів
-   [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.html) - Повертає частку зміни каскаду кандидата