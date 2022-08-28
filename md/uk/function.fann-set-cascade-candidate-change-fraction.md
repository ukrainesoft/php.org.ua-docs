Встановлює частку каскадної зміни кандидата

-   [« fann\_set\_cascade\_activation\_steepnesses](function.fann-set-cascade-activation-steepnesses.html)
    
-   [fann\_set\_cascade\_candidate\_limit »](function.fann-set-cascade-candidate-limit.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює частку каскадної зміни кандидата
    

# fannsetcascadecandidatechangefraction

(PECL fann> = 1.0.0)

fannsetcascadecandidatechangefraction - Встановлює частку каскадної зміни кандидата

### Опис

```methodsynopsis
fann_set_cascade_candidate_change_fraction(resource $ann, float $cascade_candidate_change_fraction): bool
```

Встановлює частку каскадної зміни кандидата.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_candidate_change_fraction`

Частка каскадної зміни кандидата.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.html) - Повертає частку зміни каскаду кандидата