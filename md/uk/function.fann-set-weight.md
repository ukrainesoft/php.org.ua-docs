Створення зв'язку в мережі

-   [« fann\_set\_weight\_array](function.fann-set-weight-array.html)
    
-   [fann\_shuffle\_train\_data »](function.fann-shuffle-train-data.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Створення зв'язку в мережі
    

# fannsetweight

(PECL fann> = 1.0.0)

fannsetweight — Створення зв'язку в мережі

### Опис

```methodsynopsis
fann_set_weight(    resource $ann,    int $from_neuron,    int $to_neuron,    float $weight): bool
```

Створює зв'язок у мережі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`from_neuron`

Початковий нейрон

`to_neuron`

Кінцевий нейрон

`weight`

Вага зв'язку

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.