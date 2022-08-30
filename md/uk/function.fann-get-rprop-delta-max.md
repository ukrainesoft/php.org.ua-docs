Повертає максимальний розмір кроку

-   [« fanngetrpropdecreasefactor](function.fann-get-rprop-decrease-factor.html)
    
-   [fanngetrpropdeltamin »](function.fann-get-rprop-delta-min.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає максимальний розмір кроку
    

# fanngetrpropdeltamax

(PECL fann> = 1.0.0)

fanngetrpropdeltamax — Повертає максимальний розмір кроку

### Опис

```methodsynopsis
fann_get_rprop_delta_max(resource $ann): float
```

Максимальний розмір кроку - це позитивне число, що визначає, наскільки більшим може бути максимальний розмір кроку.

Максимальне значення дельти за промовчанням становить 50.0.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Максимальний розмір кроку або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetrpropdeltamax()](function.fann-set-rprop-delta-max.html) - Встановлює максимальний розмір кроку
-   [fanngetrpropdeltamin()](function.fann-get-rprop-delta-min.html) - Повертає мінімальний розмір кроку