Отримання розміру зображення з рядка даних

-   [« getimagesize](function.getimagesize.html)
    
-   [image\_type\_to\_extension »](function.image-type-to-extension.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Отримання розміру зображення з рядка даних
    

# getimagesizefromstring

(PHP 5> = 5.4.0, PHP 7, PHP 8)

getimagesizefromstring — Отримання розміру зображення з рядка даних

### Опис

```methodsynopsis
getimagesizefromstring(string $string, array &$image_info = null): array|false
```

Функція працює ідентично функції [getimagesize()](function.getimagesize.html) з тією різницею, що **getimagesizefromstring()** приймає дані зображення у вигляді рядка як перший аргумент замість імені файлу.

Щоб дізнатися, як функція працює, зверніться до документації до функції [getimagesize()](function.getimagesize.html)

### Список параметрів

`string`

Дані зображення у вигляді рядка.

`image_info`

Дивіться [getimagesize()](function.getimagesize.html)

### Значення, що повертаються

Дивіться [getimagesize()](function.getimagesize.html)

### Приклади

**Приклад #1 Приклад використання **getimagesizefromstring()****

```php
<?php
$img = '/path/to/test.png';

// Открыть как файл
$size_info1 = getimagesize($img);

// Открыть как строку
$data       = file_get_contents($img);
$size_info2 = getimagesizefromstring($data);
?>
```

### Дивіться також

-   [getimagesize()](function.getimagesize.html) - Отримання розміру зображення