Масштабує вхідні дані до навчальних даних до вказаного діапазону

-   [« fannsave](function.fann-save.html)
    
-   [fannscaleinput »](function.fann-scale-input.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Масштабує вхідні дані до навчальних даних до вказаного діапазону
    

# fannscaleinputtraindata

(PECL fann> = 1.0.0)

fannscaleinputtraindata — Масштабує вхідні дані до навчальних даних до вказаного діапазону

### Опис

```methodsynopsis
fann_scale_input_train_data(resource $train_data, float $new_min, float $new_max): bool
```

Масштабує вхідні дані до навчальних даних до вказаного діапазону.

### Список параметрів

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_min`

Новий мінімум після масштабування вхідних даних до навчальних даних.

`new_max`

Новий максимум після масштабування вхідних даних до навчальних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannscaleoutputtraindata()](function.fann-scale-output-train-data.html) - Масштабує вихідні дані у навчальних даних до вказаного діапазону
-   [fannscaletraindata()](function.fann-scale-train-data.html) - Масштабує вхідні та вихідні дані у навчальних даних до вказаного діапазону