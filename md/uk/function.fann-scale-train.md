Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів

-   [« fann\_scale\_train\_data](function.fann-scale-train-data.html)
    
-   [fann\_set\_activation\_function\_hidden »](function.fann-set-activation-function-hidden.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів
    

# fannscaletrain

(PECL fann> = 1.0.0)

fannscaletrain — Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів

### Опис

```methodsynopsis
fann_scale_train(resource $ann, resource $train_data): bool
```

Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_descale\_train()](function.fann-descale-train.html) - Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів
-   [fann\_set\_scaling\_params()](function.fann-set-scaling-params.html) - Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання