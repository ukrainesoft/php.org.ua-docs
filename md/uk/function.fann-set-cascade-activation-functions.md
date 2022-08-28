Встановлює масив каскадних функцій активації кандидатів

-   [« fann\_set\_callback](function.fann-set-callback.html)
    
-   [fann\_set\_cascade\_activation\_steepnesses »](function.fann-set-cascade-activation-steepnesses.html)
    
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

Дивіться [fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.html) для опису того, які нейрони-кандидати будуть згенеровані цим масивом.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_activation_functions`

Масив каскадних функцій активації кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_activation\_functions\_count()](function.fann-get-cascade-activation-functions-count.html) - Повертає кількість функцій каскадної активації
-   **fannsetcascadeactivationfunctions()**