---
navigation:
  - function.fann-create-shortcut.html: « fanncreateshortcut
  - function.fann-create-sparse.html: fanncreatesparse »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanncreatesparsearray
---
# fanncreatesparsearray

(PECL fann> = 1.0.0)

fanncreatesparsearray - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена, використовуючи масив розмірів шарів

### Опис

```methodsynopsis
fann_create_sparse_array(float $connection_rate, int $num_layers, array $layers): resource
```

Створює стандартну нейронну мережу зворотного поширення, яка повністю підключена, використовуючи масив розмірів шарів.

### Список параметрів

`connection_rate`

Швидкість з'єднання визначає, скільки з'єднань буде у мережі. Якщо швидкість підключення встановлена ​​на 1, мережа буде повністю підключена, але якщо вона встановлена ​​на 0,5, буде встановлена ​​лише половина з'єднань. Швидкість з'єднання 1 дасть той же результат, що і [fanncreatestandard()](function.fann-create-standard.html)

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`layers`

Масив розмірів шарів.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanncreatesparse()](function.fann-create-sparse.html) - створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fanncreatestandard()](function.fann-create-standard.html) - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
-   [fanncreateshortcut()](function.fann-create-shortcut.html) - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
