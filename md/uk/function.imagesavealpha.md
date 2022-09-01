---
navigation:
  - function.imagerotate.html: « imagerotate
  - function.imagescale.html: imagescale »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagesavealpha
---
# imagesavealpha

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

imagesavealpha — Зберігати повну інформацію альфа-каналу при збереженні зображень PNG

### Опис

```methodsynopsis
imagesavealpha(GdImage $image, bool $enable): bool
```

**imagesavealpha()** встановлює прапор, що визначає, чи зберігатиметься повна інформація альфа-каналу (на противагу однокольоровій прозорості) та зберігає PNG зображення

Альфа-змішування має бути відключено ( `imagealphablending ($ im, false)` ), щоб альфа-канал зберігався насамперед.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`enable`

Чи потрібно зберігати альфа канал чи ні. За замовчуванням **`false`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesavealpha()****

```php
<?php
// Загрузка png изображения с альфа каналом
$png = imagecreatefrompng('./alphachannel_example.png');

// Выключение альфа-смешения
imagealphablending($png, false);

// Какие-то операции

// Установка альфа-флага
imagesavealpha($png, true);

// Вывод изображения и очистка памяти
header('Content-Type: image/png');

imagepng($png);
imagedestroy($png);
?>
```

### Дивіться також

-   [imagealphablending()](function.imagealphablending.html) - Встановлення режиму сполучення кольорів для зображення
