Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання

-   [« fann\_set\_sarprop\_weight\_decay\_shift](function.fann-set-sarprop-weight-decay-shift.html)
    
-   [fann\_set\_train\_error\_function »](function.fann-set-train-error-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання
    

# fannsetscalingparams

(PECL fann> = 1.0.0)

fannsetscalingparams — Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання

### Опис

```methodsynopsis
fann_set_scaling_params(    resource $ann,    resource $train_data,    float $new_input_min,    float $new_input_max,    float $new_output_min,    float $new_output_max): bool
```

Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_input_min`

Бажана нижня межа у вхідних даних після масштабування (суворо не дотримується)

`new_input_max`

Бажана верхня межа у вхідних даних після масштабування (суворо не дотримується)

`new_output_min`

Бажана нижня межа у вихідних даних після масштабування (суворо не дотримується)

`new_output_max`

Бажана верхня межа у вихідних даних після масштабування (суворо не дотримується)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_input\_scaling\_params()](function.fann-set-input-scaling-params.html) - розраховує вхідні параметри масштабування для майбутнього використання на основі даних навчання
-   [fann\_set\_output\_scaling\_params()](function.fann-set-output-scaling-params.html) - розраховує вихідні параметри масштабування для майбутнього використання на основі даних навчання