---
navigation:
  - function.fann-create-from-file.md: « fann\_create\_from\_file
  - function.fann-create-shortcut.md: fann\_create\_shortcut »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_create\_shortcut\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_create\_shortcut\_array

(PECL fann >= 1.0.0)

fann\_create\_shortcut\_array — Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання.

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

Повертає ресурс нейронної мережі у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_create\_shortcut()](function.fann-create-shortcut.md) \- Створює стандартну нейронну мережу зворотного розповсюдження, яка не повністю підключена та має швидкі з'єднання
-   [fann\_create\_sparse()](function.fann-create-sparse.md) \- створює стандартну нейронну мережу зворотного поширення, яка не повністю підключена
-   [fann\_create\_standard()](function.fann-create-standard.md) \- Створює стандартну повністю підключену нейронну мережу зворотного розповсюдження
