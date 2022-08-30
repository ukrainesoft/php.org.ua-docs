Встановлює частку каскадної зміни кандидата

-   [« fannsetcascadeactivationsteepnesses](function.fann-set-cascade-activation-steepnesses.html)
    
-   [fannsetcascadecandidatelimit »](function.fann-set-cascade-candidate-limit.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
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

-   [fanngetcascadecandidatechangefraction()](function.fann-get-cascade-candidate-change-fraction.html) - Повертає частку зміни каскаду кандидата