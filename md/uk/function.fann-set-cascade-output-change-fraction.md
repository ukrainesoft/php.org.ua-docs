Встановлює частку зміни каскадних вихідних даних

-   [« fann\_set\_cascade\_num\_candidate\_groups](function.fann-set-cascade-num-candidate-groups.html)
    
-   [fann\_set\_cascade\_output\_stagnation\_epochs »](function.fann-set-cascade-output-stagnation-epochs.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює частку зміни каскадних вихідних даних
    

# fannsetcascadeoutputchangefraction

(PECL fann> = 1.0.0)

fannsetcascadeoutputchangefraction - Встановлює частку зміни каскадних вихідних даних

### Опис

```methodsynopsis
fann_set_cascade_output_change_fraction(resource $ann, float $cascade_output_change_fraction): bool
```

Встановлює частку зміни каскадних вихідних даних.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_output_change_fraction`

Частка змін каскадних вихідних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_output\_change\_fraction()](function.fann-get-cascade-output-change-fraction.html) - Повертає частку зміни виходу каскаду