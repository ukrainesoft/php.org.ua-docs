Встановлює зсув згасання sarprop

-   [« fann\_set\_sarprop\_temperature](function.fann-set-sarprop-temperature.html)
    
-   [fann\_set\_scaling\_params »](function.fann-set-scaling-params.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює зсув згасання sarprop
    

# fannsetsarpropweightdecayshift

(PECL fann> = 1.0.0)

fannsetsarpropweightdecayshift - Встановлює зміщення згасання sarprop

### Опис

```methodsynopsis
fann_set_sarprop_weight_decay_shift(resource $ann, float $sarprop_weight_decay_shift): bool
```

Встановлює зміщення загасання sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_weight_decay_shift`

Зміщення загасання sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_sarprop\_weight\_decay\_shift()](function.fann-get-sarprop-weight-decay-shift.html) - Повертає зсув зменшення ваги sarprop