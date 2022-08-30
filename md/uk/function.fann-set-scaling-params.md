Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання

-   [« fannsetsarpropweightdecayshift](function.fann-set-sarprop-weight-decay-shift.html)
    
-   [fannsettrainerrorfunction »](function.fann-set-train-error-function.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
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

-   [fannsetinputscalingparams()](function.fann-set-input-scaling-params.html) - розраховує вхідні параметри масштабування для майбутнього використання на основі даних навчання
-   [fannsetoutputscalingparams()](function.fann-set-output-scaling-params.html) - розраховує вихідні параметри масштабування для майбутнього використання на основі даних навчання