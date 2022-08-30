Встановлює масив каскадних функцій активації кандидатів

-   [« fannsetcallback](function.fann-set-callback.html)
    
-   [fannsetcascadeactivationsteepnesses »](function.fann-set-cascade-activation-steepnesses.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює масив каскадних функцій активації кандидатів
    

# fannsetcascadeactivationфункцій

(PECL fann> = 1.0.0)

fannsetcascadeactivationfunctions - Встановлює масив каскадних функцій активації кандидатів

### Опис

```methodsynopsis
fann_set_cascade_activation_functions(resource $ann, array $cascade_activation_functions): bool
```

Встановлює масив каскадних функцій активації кандидатів.

Дивіться [fanngetcascadenumcandidates()](function.fann-get-cascade-num-candidates.html) для опису того, які нейрони-кандидати будуть згенеровані цим масивом.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_activation_functions`

Масив каскадних функцій активації кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetcascadeactivationfunctionscount()](function.fann-get-cascade-activation-functions-count.html) - Повертає кількість функцій каскадної активації
-   **fannsetcascadeactivationfunctions()**