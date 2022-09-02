---
navigation:
  - function.imagecreatefrombmp.md: « imagecreatefrombmp
  - function.imagecreatefromgd2part.md: imagecreatefromgd2part »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromgd2
---
# imagecreatefromgd2

(PHP 4> = 4.0.7, PHP 5, PHP 7, PHP 8)

imagecreatefromgd2 — Створення нового зображення на основі GD2 або URL

### Опис

```methodsynopsis
imagecreatefromgd2(string $filename): GdImage|false
```

Створення нового зображення на основі GD2 або URL.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була включена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до GD2 зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecreatefromgd2()****

```php
<?php
// загрузка gd2 изображения
$im = imagecreatefromgd2('./test.gd2');

// применение эффекта к изображению, этот код
// инвертирует цвета
if(function_exists('imagefilter'))
{
    imagefilter($im, IMG_FILTER_NEGATE);
}

// сохранение изображения
imagegd2($im, './test_updated.gd2');
imagedestroy($im);
?>
```

### Примітки

**Увага**

Формати зображень GD та GD2 є пропрієтарними форматами зображень libgd. Вони повинні розглядатися як *застарілі* і повинні використовуватися тільки з метою розробки та тестування.
