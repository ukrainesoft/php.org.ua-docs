---
navigation:
  - function.fann-create-standard-array.html: « fanncreatestandardarray
  - function.fann-create-train-from-callback.html: fanncreatetrainfromcallback »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncreatestandard
---
# fanncreatestandard

(PECL fann> = 1.0.0)

fanncreatestandard — Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження

### Опис

```methodsynopsis
fann_create_standard(    int $num_layers,    int $num_neurons1,    int $num_neurons2,    int ...$num_neuronsN): resource
```

Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження.

У кожному шарі буде зміщений нейрон (крім вихідного шару), і цей нейрон зміщення буде пов'язаний з усіма нейронами в наступному шарі. Працюючи в мережі вузли усунення завжди видає 1.

Щоб знищити нейронну мережу, скористайтеся функцією [fanndestroy()](function.fann-destroy.md)

### Список параметрів

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

-   [fanncreatestandardarray()](function.fann-create-standard-array.md) - Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження, використовуючи масив розмірів шарів
-   [fanncreatesparse()](function.fann-create-sparse.md) - створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fanncreateshortcut()](function.fann-create-shortcut.md) - Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
