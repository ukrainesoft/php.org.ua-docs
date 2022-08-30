Повертає зсув зменшення ваги sarprop

-   [« fanngetsarproptemperature](function.fann-get-sarprop-temperature.html)
    
-   [fanngettotalconnections »](function.fann-get-total-connections.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає зсув зменшення ваги sarprop
    

# fanngetsarpropweightdecayshift

(PECL fann> = 1.0.0)

fanngetsarpropweightdecayshift — Повертає зменшення ваги sarprop

### Опис

```methodsynopsis
fann_get_sarprop_weight_decay_shift(resource $ann): float
```

Повертає зсув зменшення ваги sarprop.

Максимальна дельта за промовчанням становить -6.644.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Зсув зменшення ваги sarprop або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannsetsarpropweightdecayshift()](function.fann-set-sarprop-weight-decay-shift.html) - Встановлює зміщення згасання sarprop