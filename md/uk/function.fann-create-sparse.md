---
navigation:
  - function.fann-create-sparse-array.html: « fanncreatesparsearray
  - function.fann-create-standard-array.html: fanncreatestandardarray »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncreatesparse
---
# fanncreatesparse

(PECL fann> = 1.0.0)

fanncreatesparse — Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена

### Опис

```methodsynopsis
fann_create_sparse(    float $connection_rate,    int $num_layers,    int $num_neurons1,    int $num_neurons2,    int ...$num_neuronsN): resource
```

Створює стандартну нейронну мережу зворотного поширення, яка повністю підключена.

### Список параметрів

`connection_rate`

Швидкість з'єднання визначає, скільки з'єднань буде в мережі. Якщо швидкість підключення встановлена ​​на 1, мережа буде повністю підключена, але якщо вона встановлена ​​на 0,5, буде встановлена ​​лише половина з'єднань. Швидкість з'єднання 1 дасть той же результат, що і [fanncreatestandard()](function.fann-create-standard.md)

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`num_neurons1`

Кількість нейронів у першому шарі.

`num_neurons2`

Кількість нейронів у другому шарі.

`num_neuronsN`

Кількість нейронів у інших шарах.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanncreatesparsearray()](function.fann-create-sparse-array.md) - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена, використовуючи масив розмірів шарів
-   [fanncreatestandard()](function.fann-create-standard.md) - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
-   [fanncreateshortcut()](function.fann-create-shortcut.md) - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
