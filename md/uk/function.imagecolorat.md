---
navigation:
  - function.imagecolorallocatealpha.md: « imagecolorallocatealpha
  - function.imagecolorclosest.md: imagecolorclosest »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorat

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorat — Отримання індексу кольору пікселя

### Опис

```methodsynopsis
imagecolorat(GdImage $image, int $x, int $y): int|false
```

Повертає індекс кольору пікселя на заданих координатах на зображенні `image`

Якщо передається truecolor-зображення, функція повертає ціле число RGB значення для пікселя. Для виділення окремих компонентів червоного, зеленого або синього каналів використовуйте бітовий зсув та маскування:

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`x`

x-координата пікселя.

`y`

y-координата пікселя.

### Значення, що повертаються

Повертає індекс кольору або \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Доступ до компонентів RGB кольору**

```php
<?php
$im = imagecreatefrompng("php.png");
$rgb = imagecolorat($im, 10, 15);
$r = ($rgb >> 16) & 0xFF;
$g = ($rgb >> 8) & 0xFF;
$b = $rgb & 0xFF;

var_dump($r, $g, $b);
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(119)
int(123)
int(180)
```

**Приклад #2 Додані RGB значення з використанням [imagecolorsforindex()](function.imagecolorsforindex.md)**

```php
<?php
$im = imagecreatefrompng("php.png");
$rgb = imagecolorat($im, 10, 15);

$colors = imagecolorsforindex($im, $rgb);

var_dump($colors);
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(4) {
  ["red"]=>
  int(119)
  ["green"]=>
  int(123)
  ["blue"]=>
  int(180)
  ["alpha"]=>
  int(127)
}
```

### Дивіться також

-   [imagecolorset()](function.imagecolorset.md) \- Встановлення набору кольорів для заданого індексу палітри
-   [imagecolorsforindex()](function.imagecolorsforindex.md) \- Отримання кольорів, що відповідають індексу
-   [imagesetpixel()](function.imagesetpixel.md) \- Малювання точки
