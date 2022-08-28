Встановлює масив крутості включення кандидатів у каскад

-   [« fann\_set\_cascade\_activation\_functions](function.fann-set-cascade-activation-functions.html)
    
-   [fann\_set\_cascade\_candidate\_change\_fraction »](function.fann-set-cascade-candidate-change-fraction.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює масив крутості включення кандидатів у каскад
    

# fannsetcascadeactivationsteepnesses

(PECL fann> = 1.0.0)

fannsetcascadeactivationsteepnesses - Встановлює масив крутості включення кандидатів у каскад

### Опис

```methodsynopsis
fann_set_cascade_activation_steepnesses(resource $ann, array $cascade_activation_steepnesses_count): bool
```

Встановлює масив крутості включення кандидатів у каскад.

Дивіться [fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.html) для опису того, які нейрони-кандидати будуть згенеровані цим масивом.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_activation_steepnesses_count`

Масив крутості включення кандидатів у каскад.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_activation\_steepnesses()](function.fann-get-cascade-activation-steepnesses.html) - Повертає крутість каскадної активації
-   [fann\_get\_cascade\_activation\_steepnesses\_count()](function.fann-get-cascade-activation-steepnesses-count.html) - Кількість крутості активації