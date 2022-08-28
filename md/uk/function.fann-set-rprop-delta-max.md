Встановлює максимальний розмір кроку

-   [« fann\_set\_rprop\_decrease\_factor](function.fann-set-rprop-decrease-factor.html)
    
-   [fann\_set\_rprop\_delta\_min »](function.fann-set-rprop-delta-min.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює максимальний розмір кроку
    

# fannsetrpropdeltamax

(PECL fann> = 1.0.0)

fannsetrpropdeltamax — Встановлює максимальний розмір кроку

### Опис

```methodsynopsis
fann_set_rprop_delta_max(resource $ann, float $rprop_delta_max): bool
```

Максимальний розмір кроку - це позитивне число, що визначає, наскільки більшим може бути максимальний розмір кроку.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_delta_max`

Максимальний розмір кроку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_rprop\_delta\_max()](function.fann-get-rprop-delta-max.html) - Повертає максимальний розмір кроку
-   [fann\_get\_rprop\_delta\_min()](function.fann-get-rprop-delta-min.html) - Повертає мінімальний розмір кроку