---
navigation:
  - function.fann-create-shortcut-array.md: « fanncreateshortcutarray
  - function.fann-create-sparse-array.md: fanncreatesparsearray »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncreateshortcut
---
# fanncreateshortcut

(PECL fann> = 1.0.0)

fanncreateshortcut — Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання.

### Опис

```methodsynopsis
fann_create_shortcut(    int $num_layers,    int $num_neurons1,    int $num_neurons2,    int ...$num_neuronsN): resource
```

Створює стандартну нейронну мережу зворотного розповсюдження, яка повністю підключена і має з'єднання швидкого доступу.

З'єднання швидкого доступу – це з'єднання, що пропускають шари. Повністю підключена мережа зі з'єднаннями швидкого доступу - це мережа, де всі нейрони пов'язані з усіма нейронами більш пізніх рівнях. Включаючи прямі з'єднання від вхідного шару до вихідного шару.

### Список параметрів

`num_layers`

Загальна кількість шарів, включаючи вхідний та вихідний шар.

`num_neurons1`

Кількість нейронів у першому шарі.

`num_neurons2`

Кількість нейронів у другому шарі.

`num_neuronsN`

Кількість нейронів у наступних шарах.

### Значення, що повертаються

Повертає ресурс нейронної мережі у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanncreateshortcutarray()](function.fann-create-shortcut-array.md) - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
-   [fanncreatesparse()](function.fann-create-sparse.md) - створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fanncreatestandard()](function.fann-create-standard.md) - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
