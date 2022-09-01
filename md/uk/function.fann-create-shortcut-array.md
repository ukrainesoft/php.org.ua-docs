---
navigation:
  - function.fann-create-from-file.html: « fanncreatefromfile
  - function.fann-create-shortcut.html: fanncreateshortcut »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanncreateshortcutarray
---
# fanncreateshortcutarray

(PECL fann> = 1.0.0)

fanncreateshortcutarray — Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання

### Опис

```methodsynopsis
fann_create_shortcut_array(int $num_layers, array $layers): resource
```

Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має з'єднання швидкого доступу з використанням масиву розмірів шарів.

### Список параметрів

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`layers`

Масив розмірів шарів.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanncreateshortcut()](function.fann-create-shortcut.html) - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
-   [fanncreatesparse()](function.fann-create-sparse.html) - створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fanncreatestandard()](function.fann-create-standard.html) - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
