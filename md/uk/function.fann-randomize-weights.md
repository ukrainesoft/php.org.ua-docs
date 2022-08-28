Надає кожному з'єднанню випадкову вагу між minweight та maxweight

-   [« fann\_print\_error](function.fann-print-error.html)
    
-   [fann\_read\_train\_from\_file »](function.fann-read-train-from-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Надає кожному з'єднанню випадкову вагу між minweight та maxweight
    

# fannrandomizeweights

(PECL fann> = 1.0.0)

fannrandomizeweights — Надає кожному з'єднанню випадкову вагу між minweight та maxweight

### Опис

```methodsynopsis
fann_randomize_weights(resource $ann, float $min_weight, float $max_weight): bool
```

Надає кожному з'єднанню випадкову вагу між `min_weight` і `max_weight`

З початку випадковий вага в діапазоні від -0,1 до 0,1.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`min_weight`

Мінімальне значення ваги.

`max_weight`

Максимальне значення ваги.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_init\_weights()](function.fann-init-weights.html) - Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen