Встановлює кількість каскадних періодів застою кандидатів

-   [« fannsetcascadecandidatelimit](function.fann-set-cascade-candidate-limit.html)
    
-   [fannsetcascademaxcandepochs »](function.fann-set-cascade-max-cand-epochs.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Встановлює кількість каскадних періодів застою кандидатів
    

# fannsetcascadecandidatestagnationepochs

(PECL fann> = 1.0.0)

fannsetcascadecandidatestagnationepochs - Встановлює кількість каскадних періодів застою кандидатів

### Опис

```methodsynopsis
fann_set_cascade_candidate_stagnation_epochs(resource $ann, int $cascade_candidate_stagnation_epochs): bool
```

Встановлює кількість каскадних періодів застою кандидатів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_candidate_stagnation_epochs`

Кількість каскадних періодів застою кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetcascadecandidatestagnationepochs()](function.fann-get-cascade-candidate-stagnation-epochs.html) - Повертає кількість періодів застою каскаду кандидата