---
navigation:
  - imagick.pingimage.html: '« Imagick::pingImage'
  - imagick.pingimagefile.html: 'Imagick::pingImageFile »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::pingImageBlob'
---
# Imagick::pingImageBlob

(PECL imagick 2, PECL imagick 3)

Imagick::pingImageBlob — Швидко витягує атрибути

### Опис

```methodsynopsis
public Imagick::pingImageBlob(string $image): bool
```

Метод можна використовувати для запиту ширини, висоти, розміру та формату зображення без зчитування всього зображення на згадку. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`image`

Рядок, що містить зображення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::pingImageBlob()****

Отримання зображення з рядка

```php
<?php
/* чтение содержимого изображения */
$image = file_get_contents("test.jpg");

/* создание нового объекта imagick */
$im = new Imagick();

/* передача строки объекту imagick */
$im->pingImageBlob($image);

/* вывод ширины и высоты изображения */
echo $im->getImageWidth() . 'x' . $im->getImageHeight();
?>
```

### Дивіться також

-   [Imagick::pingImage()](imagick.pingimage.html) - Отримує основні атрибути зображення
-   [Imagick::pingImageFile()](imagick.pingimagefile.html) - Отримує базові атрибути зображення спрощеним способом
-   [Imagick::readImage()](imagick.readimage.html) - Читає зображення із файлу
-   [Imagick::readImageBlob()](imagick.readimageblob.html) - Зчитує зображення з двійкового рядка
-   [Imagick::readImageFile()](imagick.readimagefile.html) - Читає зображення із відкритого дескриптора файлу
