Тестування набору навчальних даних та обчислення MSE для нього

-   [« fann\_subset\_train\_data](function.fann-subset-train-data.html)
    
-   [fann\_test »](function.fann-test.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Тестування набору навчальних даних та обчислення MSE для нього
    

# fanntestdata

(PECL fann> = 1.0.0)

fanntestdata — Тестування набору навчальних даних та обчислення MSE для нього

### Опис

```methodsynopsis
fann_test_data(resource $ann, resource $data): float
```

Тестування набору навчальних даних та обчислення MSE для нього.

Ця функція оновлює MSE і значення біт невдачі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Оновлена ​​MSE, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_train\_epoch()](function.fann-train-epoch.html) - Навчання протягом однієї епохи
-   [fann\_get\_bit\_fail()](function.fann-get-bit-fail.html) - Кількість бітів збою
-   [fann\_get\_MSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання