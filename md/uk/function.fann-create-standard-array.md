---
navigation:
  - function.fann-create-sparse.md: « fanncreatesparse
  - function.fann-create-standard.md: fanncreatestandard »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncreatestandardarray
---
# fanncreatestandardarray

(PECL fann> = 1.0.0)

fanncreatestandardarray - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження, використовуючи масив розмірів шарів

### Опис

```methodsynopsis
fann_create_standard_array(int $num_layers, array $layers): resource
```

Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження.

У кожному шарі буде зміщений нейрон (крім вихідного шару), і цей нейрон зміщення буде пов'язаний з усіма нейронами в наступному шарі. Працюючи в мережі вузли зміщення завжди випромінюють 1.

Щоб знищити нейронну мережу, скористайтеся функцією [fanndestroy()](function.fann-destroy.md)

### Список параметрів

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`layers`

Масив розмірів шарів.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanncreatestandard()](function.fann-create-standard.md) - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
-   [fanncreatesparse()](function.fann-create-sparse.md) - створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fanncreateshortcut()](function.fann-create-shortcut.md) - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
