Повертає температуру sarprop

-   [« fann\_get\_sarprop\_step\_error\_threshold\_factor](function.fann-get-sarprop-step-error-threshold-factor.html)
    
-   [fann\_get\_sarprop\_weight\_decay\_shift »](function.fann-get-sarprop-weight-decay-shift.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає температуру sarprop
    

# fanngetsarproptemperature

(PECL fann> = 1.0.0)

fanngetsarproptemperature - Повертає температуру sarprop

### Опис

```methodsynopsis
fann_get_sarprop_temperature(resource $ann): float
```

Повертає температуру сарprop.

Температура за промовчанням становить 0.015.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Температура sarprop або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_sarprop\_temperature()](function.fann-set-sarprop-temperature.html) - Встановлює температуру sarprop