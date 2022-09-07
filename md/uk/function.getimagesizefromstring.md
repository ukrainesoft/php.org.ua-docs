---
navigation:
  - function.getimagesize.md: « getimagesize
  - function.image-type-to-extension.md: imagetypeтоextension »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: getimagesizefromstring
---
# getimagesizefromstring

(PHP 5> = 5.4.0, PHP 7, PHP 8)

getimagesizefromstring — Отримання розміру зображення з рядка даних

### Опис

```methodsynopsis
getimagesizefromstring(string $string, array &$image_info = null): array|false
```

Функція працює ідентично функції [getimagesize()](function.getimagesize.md) з тією різницею, що **getimagesizefromstring()** приймає дані зображення у вигляді рядка як перший аргумент замість імені файлу.

Щоб дізнатися, як функція працює, зверніться до документації до функції [getimagesize()](function.getimagesize.md)

### Список параметрів

`string`

Дані зображення у вигляді рядка.

`image_info`

Дивіться [getimagesize()](function.getimagesize.md)

### Значення, що повертаються

Дивіться [getimagesize()](function.getimagesize.md)

### Приклади

**Приклад #1 Приклад використання **getimagesizefromstring()****

```php
<?php
$img = '/path/to/test.png';

// Открыть как файл
$size_info1 = getimagesize($img);

// Открыть как строку
$data       = file_get_contents($img);
$size_info2 = getimagesizefromstring($data);
?>
```

### Дивіться також

-   [getimagesize()](function.getimagesize.md) - Отримання розміру зображення
