- [«imagecolorset](function.imagecolorset.md)
- [imagecolorstotal »](function.imagecolorstotal.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Отримання кольорів, що відповідають індексу

#imagecolorsforindex

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorsforindex — Отримання кольорів, які відповідають індексу

### Опис

**imagecolorsforindex**([GdImage](class.gdimage.md) `$image`, int
`$color`): array

Отримання кольорів, які відповідають заданому індексу.

### Список параметрів

`image`
Об'єкт [GdImage](class.gdimage.md), який повертається однією з функцій
створення зображень, наприклад, такий як
[imagecreatetruecolor()](function.imagecreatetruecolor.md).

`col`
Індекс кольору.

### Значення, що повертаються

Повертає асоціативний масив з червоним, зеленим, синім та альфа.
ключами, що містить відповідні значення для заданого індексу
кольору.

### Список змін

| Версія | Опис                                                                                                                                                                                        |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0  | image тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource).                                                                                                |
| 8.0.0  | Функція **imagecolorsforindex()** тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр color поза допустимим діапазоном; раніше натомість поверталося значення **false**. |

### Приклади

**Приклад #1 Приклад використання **imagecolorsforindex()****

` <?php// відкриваємо зображення$im = imagecreatefrompng('nexen.png');// отримуємо колір$start_x = 40;$start_y = 50;$color_index = imagecolorat($im, $start_y; / робимо його удобуваним$color_tran = imagecolorsforindex($im, $color_index);// що тут ?print_r($color_tran);?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[red] => 226
[green] => 222
[blue] => 252
[alpha] => 0
)

### Дивіться також

- [imagecolorat()](function.imagecolorat.md) - Отримання індексу
кольору пікселя
- [imagecolorexact()](function.imagecolorexact.md) - Отримання
індексу заданого кольору
