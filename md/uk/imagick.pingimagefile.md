---
navigation:
  - imagick.pingimageblob.html: '« Imagick::pingImageBlob'
  - imagick.polaroidimage.html: 'Imagick::polaroidImage »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::pingImageFile'
---
# Imagick::pingImageFile

(PECL imagick 2, PECL imagick 3)

Imagick::pingImageFile — Отримує базові атрибути зображення спрощеним способом

### Опис

```methodsynopsis
public Imagick::pingImageFile(resource $filehandle, string $fileName = ?): bool
```

Метод можна використовувати для запиту ширини, висоти, розміру та формату зображення без зчитування всього зображення на згадку. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`filehandle`

Відкритий дескриптор файлу зображення.

`fileName`

Необов'язкова назва файлу для цього зображення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::pingImageFile()****

Відкриття віддаленої локації

```php
<?php
/* Открытие удалённой локации с помощью fopen */
$fp = fopen("http://example.com/test.jpg");

/* Создание нового объекта Imagick */
$im = new Imagick();

/* Передача дескриптора объекту Imagick */
$im->pingImageFile($fp);
?>
```

### Дивіться також

-   [Imagick::pingImage()](imagick.pingimage.html) - Отримує основні атрибути зображення
-   [Imagick::pingImageBlob()](imagick.pingimageblob.html) - Швидко витягує атрибути
-   [Imagick::readImage()](imagick.readimage.html) - Читає зображення із файлу
-   [Imagick::readImageBlob()](imagick.readimageblob.html) - Зчитує зображення з двійкового рядка
-   [Imagick::readImageFile()](imagick.readimagefile.html) - Читає зображення із відкритого дескриптора файлу
