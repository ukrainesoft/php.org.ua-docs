Встановлює коефіцієнт зменшення під час навчання RPROP

-   [« fann\_set\_quickprop\_mu](function.fann-set-quickprop-mu.html)
    
-   [fann\_set\_rprop\_delta\_max »](function.fann-set-rprop-delta-max.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює коефіцієнт зменшення під час навчання RPROP
    

# fannsetrpropdecreasefactor

(PECL fann> = 1.0.0)

fannsetrpropdecreasefactor — Встановлює коефіцієнт зменшення під час навчання RPROP

### Опис

```methodsynopsis
fann_set_rprop_decrease_factor(resource $ann, float $rprop_decrease_factor): bool
```

Встановлює коефіцієнт зменшення під час навчання RPROP.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_decrease_factor`

Коефіцієнт зменшення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_rprop\_decrease\_factor()](function.fann-get-rprop-decrease-factor.html) - Повертає коефіцієнт зменшення під час навчання RPROP