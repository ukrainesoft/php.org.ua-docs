Кількість крутості активації

-   [« fann\_get\_cascade\_activation\_functions](function.fann-get-cascade-activation-functions.html)
    
-   [fann\_get\_cascade\_activation\_steepnesses »](function.fann-get-cascade-activation-steepnesses.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Кількість крутості активації
    

# fanngetcascadeactivationsteepnessescount

(PECL fann> = 1.0.0)

fanngetcascadeactivationsteepnessescount — Кількість крутості активації

### Опис

```methodsynopsis
fann_get_cascade_activation_steepnesses_count(resource $ann): int
```

Кількість крутості активації в масиві [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.html)

Кількість крутизни за замовчуванням активації - 4.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість крутості активації або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_steepnesses()](function.fann-get-cascade-activation-steepnesses.html) - Повертає крутість каскадної активації
-   [fann\_set\_cascade\_activation\_functions()](function.fann-set-cascade-activation-functions.html) - встановлює масив каскадних функцій активації кандидатів