Отримання індексу кольору пікселя

-   [« imagecolorallocatealpha](function.imagecolorallocatealpha.html)
    
-   [imagecolorclosest »](function.imagecolorclosest.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Отримання індексу кольору пікселя
    

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

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`x`

x-координата пікселя.

`y`

y-координата пікселя.

### Значення, що повертаються

Повертає індекс кольору або **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Описание                                                                                         |
|--------|--------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Доступ до компонентів RGB кольору**

```php
<?php
$im = imagecreatefrompng("php.png");
$rgb = imagecolorat($im, 10, 15);
$r = ($rgb >> 16) & 0xFF;
$g = ($rgb >> 8) & 0xFF;
$b = $rgb & 0xFF;

var_dump($r, $g, $b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(119)
int(123)
int(180)
```

**Приклад #2 Додані RGB значення з використанням [imagecolorsforindex()](function.imagecolorsforindex.html)**

```php
<?php
$im = imagecreatefrompng("php.png");
$rgb = imagecolorat($im, 10, 15);

$colors = imagecolorsforindex($im, $rgb);

var_dump($colors);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [imagecolorset()](function.imagecolorset.html) - Встановлення набору кольорів для заданого індексу палітри
-   [imagecolorsforindex()](function.imagecolorsforindex.html) - Отримання кольорів, що відповідають індексу
-   [imagesetpixel()](function.imagesetpixel.html) - Малювання точки