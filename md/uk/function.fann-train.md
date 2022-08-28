Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом

-   [« fann\_train\_on\_file](function.fann-train-on-file.html)
    
-   [FANNConnection »](class.fannconnection.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом
    

# fanntrain

(PECL fann> = 1.0.0)

fanntrain — Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом

### Опис

```methodsynopsis
fann_train(resource $ann, array $input, array $desired_output): bool
```

Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом. Це навчання завжди інкрементальне, тому що представлена ​​лише одна модель.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input`

Масив вхідних даних. Розмір масиву має точно відповідати [fann\_get\_num\_input()](function.fann-get-num-input.html)

`desired_output`

Масив бажаних результатів. Розмір масиву має точно відповідати [fann\_get\_num\_output()](function.fann-get-num-output.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_train\_epoch()](function.fann-train-epoch.html) - Навчання протягом однієї епохи
-   [fann\_get\_num\_input()](function.fann-get-num-input.html) - Отримує кількість вхідних нейронів
-   [fann\_get\_num\_output()](function.fann-get-num-output.html) - Отримує кількість вихідних нейронів