Повертає функції каскадної активації

-   [« fann\_get\_cascade\_activation\_functions\_count](function.fann-get-cascade-activation-functions-count.html)
    
-   [fann\_get\_cascade\_activation\_steepnesses\_count »](function.fann-get-cascade-activation-steepnesses-count.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає функції каскадної активації
    

# fanngetcascadeactivationфункцій

(PECL fann> = 1.0.0)

fanngetcascadeactivationfunctions — Повертає функції каскадної активації

### Опис

```methodsynopsis
fann_get_cascade_activation_functions(resource $ann): array
```

Масив функцій каскадної активації – це масив різних функцій активації, які використовуються кандидатами.

Дивіться [fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.html) для опису того, які нейрони кандидата генеруватимуться цим масивом.

Функції активації за замовчуванням: **`FANN_SIGMOID`** **`FANN_SIGMOID_SYMMETRIC`** **`FANN_GAUSSIAN`** **`FANN_GAUSSIAN_SYMMETRIC`** **`FANN_ELLIOT`** **`FANN_ELLIOT_SYMMETRIC`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Функції каскадної активації або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_functions\_count()](function.fann-get-cascade-activation-functions-count.html) - Повертає кількість функцій каскадної активації
-   [fann\_set\_cascade\_activation\_functions()](function.fann-set-cascade-activation-functions.html) - встановлює масив каскадних функцій активації кандидатів