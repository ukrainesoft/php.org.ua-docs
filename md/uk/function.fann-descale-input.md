Масштабує дані у вхідному векторі після отримання їх на основі раніше розрахованих параметрів

-   [« fanncreatetrain](function.fann-create-train.html)
    
-   [fanndescaleoutput »](function.fann-descale-output.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Масштабує дані у вхідному векторі після отримання їх на основі раніше розрахованих параметрів
    

# fanndescaleinput

(PECL fann> = 1.0.0)

fanndescaleinput — Масштабує дані у вхідному векторі після отримання на основі раніше розрахованих параметрів

### Опис

```methodsynopsis
fann_descale_input(resource $ann, array $input_vector): bool
```

Масштабує дані у вхідному векторі після отримання на основі раніше розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input_vector`

Вхідний вектор, який буде масштабовано

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannscaleinput()](function.fann-scale-input.html) - Масштабує дані у вхідному векторі перед подачею їх у ann на основі раніше розрахованих параметрів
-   [fanndescaleoutput()](function.fann-descale-output.html) - Масштабує дані у вихідному векторі після отримання їх на основі раніше розрахованих параметрів