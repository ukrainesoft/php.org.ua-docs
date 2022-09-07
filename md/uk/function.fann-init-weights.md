---
navigation:
  - function.fann-get-training-algorithm.md: « fanngettrainingalgorithm
  - function.fann-length-train-data.md: fannlengthtraindata »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanninitweights
---
# fanninitweights

(PECL fann> = 1.0.0)

fanninitweights - Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen

### Опис

```methodsynopsis
fann_init_weights(resource $ann, resource $train_data): bool
```

Ініціалізує ваги за допомогою алгоритму Widrow+Nguyen.

Функція поводиться аналогічно [fannrandomizeweights()](function.fann-randomize-weights.md). Вона використовуватиме алгоритм, розроблений Дерріком Нгуєном і Бернардом Відроу, щоб встановити ваги таким чином, щоб прискорити навчання. Метод не завжди буває успішним, а в деяких випадках може бути менш ефективним, ніж суто випадкова ініціалізація.

Алгоритм вимагає доступу до діапазону вхідних даних (наприклад, найбільших та найменших вхідних даних) і, отже, приймає другий аргумент, data, який є навчальними даними, які будуть використовуватися для навчання мережі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannrandomizeweights()](function.fann-randomize-weights.md) - Надає кожному з'єднанню випадкову вагу між minweight та maxweight
-   [fannreadtrainfromfile()](function.fann-read-train-from-file.md) - Читає файл, у якому зберігаються дані навчання
