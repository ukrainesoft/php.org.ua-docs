Тестування з набором вхідних даних та бажаним результатом

-   [« fann\_test\_data](function.fann-test-data.html)
    
-   [fann\_train\_epoch »](function.fann-train-epoch.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Тестування з набором вхідних даних та бажаним результатом
    

# fanntest

(PECL fann> = 1.0.0)

fanntest — Тестування з набором вхідних даних та бажаним результатом

### Опис

```methodsynopsis
fann_test(resource $ann, array $input, array $desired_output): array
```

Тестування з набором вхідних даних та бажаним результатом. Ця операція оновить середньоквадратичну помилку, але не змінить мережу.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input`

Масив вхідних даних. Розмір масиву має точно відповідати [fann\_get\_num\_input()](function.fann-get-num-input.html)

`desired_output`

Масив бажаних результатів. Розмір масиву має точно відповідати [fann\_get\_num\_output()](function.fann-get-num-output.html)

### Значення, що повертаються

Повертає тестові висновки у разі успішного виконання або **`false`** у разі виникнення помилки

### Дивіться також

-   [fann\_test\_data()](function.fann-test-data.html) - Тестування набору навчальних даних та обчислення MSE для нього
-   [fann\_train()](function.fann-train.html) - Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом
-   [fann\_get\_num\_input()](function.fann-get-num-input.html) - Отримує кількість вхідних нейронів
-   [fann\_get\_num\_output()](function.fann-get-num-output.html) - Отримує кількість вихідних нейронів