Повертає мінімальний розмір кроку

-   [« fann\_get\_rprop\_delta\_max](function.fann-get-rprop-delta-max.html)
    
-   [fann\_get\_rprop\_delta\_zero »](function.fann-get-rprop-delta-zero.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає мінімальний розмір кроку
    

# fanngetrpropdeltamin

(PECL fann> = 1.0.0)

fanngetrpropdeltamin — Повертає мінімальний розмір кроку

### Опис

```methodsynopsis
fann_get_rprop_delta_min(resource $ann): float
```

Мінімальний розмір кроку - це невелике позитивне число, що визначає, наскільки невеликим може бути мінімальний розмір кроку.

Значення дельти за умовчанням min дорівнює 0.0.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Мінімальний розмір кроку або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_rprop\_delta\_min()](function.fann-set-rprop-delta-min.html) - Встановлює мінімальний розмір кроку