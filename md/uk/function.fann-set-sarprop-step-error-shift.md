Встановлює зрушення помилки кроку sarprop

-   [« fann\_set\_rprop\_increase\_factor](function.fann-set-rprop-increase-factor.html)
    
-   [fann\_set\_sarprop\_step\_error\_threshold\_factor »](function.fann-set-sarprop-step-error-threshold-factor.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює зрушення помилки кроку sarprop
    

# fannsetsarpropsteperrorshift

(PECL fann> = 1.0.0)

fannsetsarpropsteperrorshift - Встановлює зрушення помилки кроку sarprop

### Опис

```methodsynopsis
fann_set_sarprop_step_error_shift(resource $ann, float $sarprop_step_error_shift): bool
```

Встановлює зрушення помилки кроку sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_step_error_shift`

Зрушення помилки кроку sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_sarprop\_step\_error\_shift()](function.fann-get-sarprop-step-error-shift.html) - Повертає зрушення помилки кроку sarprop