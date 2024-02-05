---
navigation:
  - function.imagerotate.md: « imagerotate
  - function.imagescale.md: imagescale »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesavealpha
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagesavealpha

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

imagesavealpha — Зберігати повну інформацію альфа-каналу під час збереження зображень

### Опис

```methodsynopsis
imagesavealpha(GdImage $image, bool $enable): bool
```

**imagesavealpha()** встановлює прапор, що визначає, чи зберігатиметься повна інформація альфа-каналу (на противагу одноколірній прозорості) і зберігає зображення. Підтримується тільки для форматів зображень, які містять повну інформацію про альфа-канал, тобто . `PNG` `WebP`и`AVIF`

> **Зауваження**: Функция**imagesavealpha()** має сенс лише для зображень `PNG`, оскільки для `WebP`и`AVIF` завжди зберігається повний альфа-канал. Не рекомендується покладатися цього поведінка, оскільки він може змінитися у майбутньому. Таким чином, функцію **imagesavealpha()** слід навмисно викликати також для зображень `WebP`и`AVIF`

Альфа-змішування має бути відключено (`imagealphablending($im, false)`), щоб альфа-канал зберігався насамперед.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`enable`

Чи потрібно зберігати альфа канал чи ні. За замовчуванням **`false`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Пример использования**imagesavealpha()\*\*\*\*

```php
<?php
// Загрузка png изображения с альфа каналом
$png = imagecreatefrompng('./alphachannel_example.png');

// Выключение альфа-смешения
imagealphablending($png, false);

// Какие-то операции

// Установка альфа-флага
imagesavealpha($png, true);

// Вывод изображения и очистка памяти
header('Content-Type: image/png');

imagepng($png);
imagedestroy($png);
?>
```

### Дивіться також

-   [imagealphablending()](function.imagealphablending.md) \- Встановлення режиму сполучення кольорів для зображення
