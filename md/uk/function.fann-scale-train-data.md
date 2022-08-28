Масштабує вхідні та вихідні дані в навчальних даних до вказаного діапазону

-   [« fann\_scale\_output](function.fann-scale-output.html)
    
-   [fann\_scale\_train »](function.fann-scale-train.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Масштабує вхідні та вихідні дані в навчальних даних до вказаного діапазону
    

# fannscaletraindata

(PECL fann> = 1.0.0)

fannscaletraindata — Масштабує вхідні та вихідні дані в навчальних даних до вказаного діапазону

### Опис

```methodsynopsis
fann_scale_train_data(resource $train_data, float $new_min, float $new_max): bool
```

Масштабує вхідні та вихідні дані у навчальних даних до вказаного діапазону.

### Список параметрів

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_min`

Новий мінімум після масштабування вхідних та вихідних даних у навчальних даних.

`new_max`

Новий максимум після масштабування вхідних та вихідних даних у навчальних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_scale\_output\_train\_data()](function.fann-scale-output-train-data.html) - Масштабує вихідні дані у навчальних даних до вказаного діапазону
-   [fann\_scale\_input\_train\_data()](function.fann-scale-input-train-data.html) - Масштабує вхідні дані до навчальних даних до вказаного діапазону