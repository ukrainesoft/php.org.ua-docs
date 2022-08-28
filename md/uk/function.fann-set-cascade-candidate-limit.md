Встановлює ліміт кандидатів

-   [« fann\_set\_cascade\_candidate\_change\_fraction](function.fann-set-cascade-candidate-change-fraction.html)
    
-   [fann\_set\_cascade\_candidate\_stagnation\_epochs »](function.fann-set-cascade-candidate-stagnation-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює ліміт кандидатів
    

# fannsetcascadecandidatelimit

(PECL fann> = 1.0.0)

fannsetcascadecandidatelimit - Встановлює ліміт кандидатів

### Опис

```methodsynopsis
fann_set_cascade_candidate_limit(resource $ann, float $cascade_candidate_limit): bool
```

Встановлює ліміт кандидатів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_candidate_limit`

Ліміт кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_candidate\_limit()](function.fann-get-cascade-candidate-limit.html) - Повертає межу кандидата