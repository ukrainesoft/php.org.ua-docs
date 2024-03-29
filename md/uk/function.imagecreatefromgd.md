---
navigation:
  - function.imagecreatefromgd2part.md: « imagecreatefromgd2part
  - function.imagecreatefromgif.md: imagecreatefromgif »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromgd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromgd

(PHP 4 >= 4.0.7, PHP 5, PHP 7, PHP 8)

imagecreatefromgd — Створення нового зображення на основі файлу GD або URL

### Опис

```methodsynopsis
imagecreatefromgd(string $filename): GdImage|false
```

Створення нового зображення на основі файлу GD або URL.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до файлу GD.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання** imagecreatefromgd()\*\*\*\*

```php
<?php
// загрузка изображения
$im = @imagecreatefromgd('./test.gd');

// проверка, загрузилось ли изображение
if(!$im)
{
     die('Не удалось загрузить изображение!');
}

// Операции с изображением можно осуществить здесь

// Сохранение изображения
imagegd($im, './test_updated.gd');
imagedestroy($im);
?>
```

### Примітки

**Увага**

Формати зображень GD та GD2 є пропрієтарними форматами зображень libgd. Вони повинні розглядатися як *застарілі* і повинні використовуватися тільки з метою розробки та тестування.
