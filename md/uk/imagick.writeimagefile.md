---
navigation:
  - imagick.writeimage.md: '« Imagick::writeImage'
  - imagick.writeimages.md: 'Imagick::writeImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::writeImageFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::writeImageFile

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::writeImageFile — Записує зображення до файлу

### Опис

```methodsynopsis
public Imagick::writeImageFile(resource $filehandle, string $format = ?): bool
```

Записує зображення у заданий файловий дескриптор. Дескриптор має бути попередньо відкритий, наприклад, за допомогою fopen. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`filehandle`

Файловий дескриптор.

`format`

Формат зображення. Список допустимих специфікаторів формату залежить від скомпілюваного набору функцій програми ImageMagick і може бути запитаний під час виконання за допомогою методу [Imagick::queryFormats()](imagick.queryformats.md)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::queryFormats()](imagick.queryformats.md) \- Повертає формати, що підтримуються Imagick
