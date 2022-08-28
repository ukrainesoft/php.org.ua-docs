Створення зв'язків у мережі

-   [« fann\_set\_training\_algorithm](function.fann-set-training-algorithm.html)
    
-   [fann\_set\_weight »](function.fann-set-weight.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Створення зв'язків у мережі
    

# fannsetweightarray

(PECL fann> = 1.0.0)

fannsetweightarray — Створення зв'язків у мережі

### Опис

```methodsynopsis
fann_set_weight_array(resource $ann, array $connections): bool
```

Створення зв'язків у мережі.

Можуть бути змінені лише вагові коефіцієнти, що не існують у мережі зв'язку та ваги ігноруватимуться.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`connections`

Масив об'єктів [FANNConnection](class.fannconnection.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.