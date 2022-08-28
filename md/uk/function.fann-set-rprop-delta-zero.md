Встановлює початковий розмір кроку

-   [« fann\_set\_rprop\_delta\_min](function.fann-set-rprop-delta-min.html)
    
-   [fann\_set\_rprop\_increase\_factor »](function.fann-set-rprop-increase-factor.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює початковий розмір кроку
    

# fannsetrpropdeltazero

(PECL fann> = 1.0.0)

fannsetrpropdeltazero — Встановлює початковий розмір кроку

### Опис

```methodsynopsis
fann_set_rprop_delta_zero(resource $ann, float $rprop_delta_zero): bool
```

Початковий розмір кроку - це позитивне число, що визначає початковий розмір кроку.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_delta_zero`

Початковий розмір кроку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_rprop\_delta\_zero()](function.fann-get-rprop-delta-zero.html) - Повертає початковий розмір кроку
-   [fann\_get\_rprop\_delta\_min()](function.fann-get-rprop-delta-min.html) - Повертає мінімальний розмір кроку
-   [fann\_get\_rprop\_delta\_max()](function.fann-get-rprop-delta-max.html) - Повертає максимальний розмір кроку