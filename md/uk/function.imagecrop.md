Обрізати зображення до заданого прямокутника

-   [« imagecreatetruecolor](function.imagecreatetruecolor.md)
    
-   [imagecropauto »](function.imagecropauto.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Обрізати зображення до заданого прямокутника
    

# imagecrop

(PHP 5> = 5.5.0, PHP 7, PHP 8)

imagecrop — Обрізати зображення до прямокутника.

### Опис

```methodsynopsis
imagecrop(GdImage $image, array $rectangle): GdImage|false
```

Обрізає зображення до заданої прямокутної області та повертає отримане зображення. Заданий параметр `image` не змінюється.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`rectangle`

Обрізаний прямокутник у вигляді масиву (array) із ключами `x` `y` `width` і `height`

### Значення, що повертаються

Повертає об'єкт обрізаного зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecrop()****

У цьому прикладі показано, як обрізати зображення до квадратної області.

```php
<?php
$im = imagecreatefrompng('example.png');
$size = min(imagesx($im), imagesy($im));
$im2 = imagecrop($im, ['x' => 0, 'y' => 0, 'width' => $size, 'height' => $size]);
if ($im2 !== FALSE) {
    imagepng($im2, 'example-cropped.png');
    imagedestroy($im2);
}
imagedestroy($im);
?>
```

### Дивіться також

-   [imagecropauto()](function.imagecropauto.md) - Обрізає зображення автоматично, використовуючи один із доступних режимів