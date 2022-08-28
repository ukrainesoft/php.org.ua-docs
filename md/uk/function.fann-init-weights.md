Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen

-   [« fann\_get\_training\_algorithm](function.fann-get-training-algorithm.html)
    
-   [fann\_length\_train\_data »](function.fann-length-train-data.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen
    

# fanninitweights

(PECL fann> = 1.0.0)

fanninitweights - Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen

### Опис

```methodsynopsis
fann_init_weights(resource $ann, resource $train_data): bool
```

Ініціалізує ваги за допомогою алгоритму Widrow+Nguyen.

Функція поводиться аналогічно [fann\_randomize\_weights()](function.fann-randomize-weights.html). Вона використовуватиме алгоритм, розроблений Дерріком Нгуєном і Бернардом Відроу, щоб встановити ваги таким чином, щоб прискорити навчання. Метод не завжди буває успішним, а в деяких випадках може бути менш ефективним, ніж суто випадкова ініціалізація.

Алгоритм вимагає доступу до діапазону вхідних даних (наприклад, найбільших та найменших вхідних даних) і, отже, приймає другий аргумент, data, який є навчальними даними, які будуть використовуватися для навчання мережі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_randomize\_weights()](function.fann-randomize-weights.html) - Надає кожному з'єднанню випадкову вагу між minweight та maxweight
-   [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.html) - Читає файл, у якому зберігаються дані навчання