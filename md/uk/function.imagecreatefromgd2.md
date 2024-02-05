---
navigation:
  - function.imagecreatefrombmp.md: « imagecreatefrombmp
  - function.imagecreatefromgd2part.md: imagecreatefromgd2part »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromgd2
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromgd2

(PHP 4 >= 4.0.7, PHP 5, PHP 7, PHP 8)

imagecreatefromgd2 — Створення нового зображення на основі GD2 або URL

### Опис

```methodsynopsis
imagecreatefromgd2(string $filename): GdImage|false
```

Створення нового зображення на основі GD2 або URL.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до GD2 зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**imagecreatefromgd2()\*\*\*\*

```php
<?php
// загрузка gd2 изображения
$im = imagecreatefromgd2('./test.gd2');

// применение эффекта к изображению, этот код
// инвертирует цвета
if(function_exists('imagefilter'))
{
    imagefilter($im, IMG_FILTER_NEGATE);
}

// сохранение изображения
imagegd2($im, './test_updated.gd2');
imagedestroy($im);
?>
```

### Примітки

**Увага**

Формати зображень GD та GD2 є пропрієтарними форматами зображень libgd. Вони повинні розглядатися як *застарілі* і повинні використовуватися тільки з метою розробки та тестування.
