Встановлює пороговий коефіцієнт помилки кроку sarprop

-   [« fannsetsarpropsteperrorshift](function.fann-set-sarprop-step-error-shift.html)
    
-   [fannsetsarproptemperature »](function.fann-set-sarprop-temperature.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює пороговий коефіцієнт помилки кроку sarprop
    

# fannsetsarpropsteperrorthresholdfactor

(PECL fann> = 1.0.0)

fannsetsarpropsteperrorthresholdfactor — Встановлює пороговий коефіцієнт помилки кроку sarprop

### Опис

```methodsynopsis
fann_set_sarprop_step_error_threshold_factor(resource $ann, float $sarprop_step_error_threshold_factor): bool
```

Встановлює пороговий коефіцієнт помилки кроку sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_step_error_threshold_factor`

Пороговий коефіцієнт помилки кроку sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fanngetsarpropsteperrorthresholdfactor()](function.fann-get-sarprop-step-error-threshold-factor.html) - Повертає пороговий коефіцієнт помилки кроку sarprop