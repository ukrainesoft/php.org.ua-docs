Повертає кількість функцій каскадної активації

-   [« fann\_get\_bit\_fail](function.fann-get-bit-fail.html)
    
-   [fann\_get\_cascade\_activation\_functions »](function.fann-get-cascade-activation-functions.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає кількість функцій каскадної активації
    

# fanngetcascadeactivationфункційcount

(PECL fann> = 1.0.0)

fanngetcascadeactivationфункційcount — Повертає кількість функцій каскадної активації

### Опис

```methodsynopsis
fann_get_cascade_activation_functions_count(resource $ann): int
```

Кількість функцій активації у масиві [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.html)

Кількість функцій активації за промовчанням - 6.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість функцій каскадної активації або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.html) - Повертає функції каскадної активації
-   [fann\_set\_cascade\_activation\_functions()](function.fann-set-cascade-activation-functions.html) - встановлює масив каскадних функцій активації кандидатів