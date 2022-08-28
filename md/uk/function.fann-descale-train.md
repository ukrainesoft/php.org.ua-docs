Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів

-   [« fann\_descale\_output](function.fann-descale-output.html)
    
-   [fann\_destroy\_train »](function.fann-destroy-train.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів
    

# fanndescaletrain

(PECL fann> = 1.0.0)

fanndescaletrain — Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів

### Опис

```methodsynopsis
fann_descale_train(resource $ann, resource $train_data): bool
```

Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_scale\_train()](function.fann-scale-train.html) - Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів
-   [fann\_set\_scaling\_params()](function.fann-set-scaling-params.html) - Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання