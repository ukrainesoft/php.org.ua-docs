---
navigation:
  - function.fann-get-training-algorithm.md: « fann\_get\_training\_algorithm
  - function.fann-length-train-data.md: fann\_length\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_init\_weights
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_init\_weights

(PECL fann >= 1.0.0)

fann\_init\_weights - Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen

### Опис

```methodsynopsis
fann_init_weights(resource $ann, resource $train_data): bool
```

Ініціалізує ваги за допомогою алгоритму Widrow+Nguyen.

Функція поводиться аналогічно [fann\_randomize\_weights()](function.fann-randomize-weights.md). Вона використовуватиме алгоритм, розроблений Дерріком Нгуєном і Бернардом Відроу, щоб встановити ваги таким чином, щоб прискорити навчання. Метод не завжди буває успішним, а в деяких випадках може бути менш ефективним, ніж суто випадкова ініціалізація.

Алгоритм вимагає доступу до діапазону вхідних даних (наприклад, найбільших і найменших вхідних даних) і, отже, приймає другий аргумент, data, який є навчальними даними, які будуть використовуватися для навчання мережі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_randomize\_weights()](function.fann-randomize-weights.md) \- Надає кожному з'єднанню випадкову вагу між min\_weight та max\_weight
-   [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.md) \- Читає файл, у якому зберігаються дані навчання
