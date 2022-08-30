Повертає пороговий коефіцієнт помилки кроку sarprop

-   [« fanngetsarpropsteperrorshift](function.fann-get-sarprop-step-error-shift.html)
    
-   [fanngetsarproptemperature »](function.fann-get-sarprop-temperature.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Повертає пороговий коефіцієнт помилки кроку sarprop
    

# fanngetsarpropsteperrorthresholdfactor

(PECL fann> = 1.0.0)

fanngetsarpropsteperrorthresholdfactor - Повертає пороговий коефіцієнт помилки кроку sarprop

### Опис

```methodsynopsis
fann_get_sarprop_step_error_threshold_factor(resource $ann): float
```

Повертає пороговий коефіцієнт помилки кроку sarprop.

Коефіцієнт за замовчуванням становить 0,1.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Пороговий коефіцієнт помилки кроку або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannsetsarpropsteperrorthresholdfactor()](function.fann-set-sarprop-step-error-threshold-factor.html) - Встановлює пороговий коефіцієнт помилки кроку sarprop