Встановлює температуру sarprop

-   [« fann\_set\_sarprop\_step\_error\_threshold\_factor](function.fann-set-sarprop-step-error-threshold-factor.html)
    
-   [fann\_set\_sarprop\_weight\_decay\_shift »](function.fann-set-sarprop-weight-decay-shift.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює температуру sarprop
    

# fannsetsarproptemperature

(PECL fann> = 1.0.0)

fannsetsarproptemperature - Встановлює температуру sarprop

### Опис

```methodsynopsis
fann_set_sarprop_temperature(resource $ann, float $sarprop_temperature): bool
```

Встановлює температуру sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_temperature`

Температура сарprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_sarprop\_temperature()](function.fann-get-sarprop-temperature.html) - Повертає температуру sarprop