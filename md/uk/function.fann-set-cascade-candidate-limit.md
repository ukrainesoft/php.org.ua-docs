Встановлює ліміт кандидатів

-   [« fannsetcascadecandidatechangefraction](function.fann-set-cascade-candidate-change-fraction.html)
    
-   [fannsetcascadecandidatestagnationepochs »](function.fann-set-cascade-candidate-stagnation-epochs.html)
    
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

-   [fanngetcascadecandidatelimit()](function.fann-get-cascade-candidate-limit.html) - Повертає межу кандидата