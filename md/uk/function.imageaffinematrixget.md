---
navigation:
  - function.imageaffinematrixconcat.md: « imageaffinematrixconcat
  - function.imagealphablending.md: imagealphablending »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageaffinematrixget
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imageaffinematrixget

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

imageaffinematrixget — Отримує матрицю афінного перетворення

### Опис

```methodsynopsis
imageaffinematrixget(int $type, array|float $options): array|false
```

Повертає матрицю афінного перетворення.

### Список параметрів

`type`

Одна из констант\*\*`IMG_AFFINE_*`\*\*

`options`

Якщо `type`равен\*\*`IMG_AFFINE_TRANSLATE`**или**`IMG_AFFINE_SCALE`\*\* `options` має бути масивом (array) з ключами `x`и`y`обидва мають значення типу float.

Якщо `type`равен\*\*`IMG_AFFINE_ROTATE`\*\* **`IMG_AFFINE_SHEAR_HORIZONTAL`**или**`IMG_AFFINE_SHEAR_VERTICAL`** `options` повинен бути числом з плаваючою точкою (float), що визначає кут.

### Значення, що повертаються

Матриця афінного перетворення (масив із ключами від до`5` і значеннями з плаваючою точкою) або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**imageaffinematrixget()\*\*\*\*

```php
<?php
$matrix = imageaffinematrixget(IMG_AFFINE_TRANSLATE, array('x' => 2, 'y' => 3));
print_r($matrix);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => 1
    [1] => 0
    [2] => 0
    [3] => 1
    [4] => 2
    [5] => 3
)
```

### Дивіться також

-   [imageaffine()](function.imageaffine.md) \- Повернути зображення, що містить афінно-перетворене зображення src, використовуючи додаткову область обмеження
-   [imageaffinematrixconcat()](function.imageaffinematrixconcat.md) \- Конкатенує дві афінні матриці перетворення
