---
navigation:
  - function.imageaffine.md: « imageaffine
  - function.imageaffinematrixget.md: imageaffinematrixget »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageaffinematrixconcat
---
# imageaffinematrixconcat

(PHP 5> = 5.5.0, PHP 7, PHP 8)

imageaffinematrixconcat — Конкатенує дві афінні матриці перетворення

### Опис

```methodsynopsis
imageaffinematrixconcat(array $matrix1, array $matrix2): array|false
```

Повертає конкатенацію двох афінних матриць перетворення, що корисно, якщо кілька перетворень повинні бути застосовані до одного й того самого зображення за один раз.

### Список параметрів

`matrix1`

Афінна матриця перетворення (масив із ключами від `0` до `5` та значеннями з плаваючою точкою).

`matrix2`

Афінна матриця перетворення (масив із ключами від `0` до `5` та значеннями з плаваючою точкою).

### Значення, що повертаються

Афінна матриця перетворення (масив із ключами від `0` до `5` і значеннями з плаваючою точкою) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **imageaffinematrixconcat()****

```php
<?php
$m1 = imageaffinematrixget(IMG_AFFINE_TRANSLATE, array('x' => 2, 'y' => 3));
$m2 = imageaffinematrixget(IMG_AFFINE_SCALE, array('x' => 4, 'y' => 5));
$matrix = imageaffinematrixconcat($m1, $m2);
print_r($matrix);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => 4
    [1] => 0
    [2] => 0
    [3] => 5
    [4] => 8
    [5] => 15
)
```

### Дивіться також

-   [imageaffine()](function.imageaffine.md) - Повернути зображення, що містить афінно-перетворене зображення src, використовуючи додаткову область обмеження
-   [imageaffinematrixget()](function.imageaffinematrixget.md) - Отримує матрицю афінного перетворення
