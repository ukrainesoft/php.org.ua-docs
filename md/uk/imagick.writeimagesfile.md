Записує кадри у файловий дескриптор

-   [« Imagick::writeImages](imagick.writeimages.md)
    
-   [ImagickDraw »](class.imagickdraw.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Записує кадри у файловий дескриптор
    

# Imagick::writeImagesFile

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::writeImagesFile — Записує кадри у файловий дескриптор

### Опис

```methodsynopsis
public Imagick::writeImagesFile(resource $filehandle, string $format = ?): bool
```

Записує всі кадри зображення у відкритий дескриптор файлу. Метод можна використовувати для запису анімованих файлів GIF або інших багатокадрових зображень у відкритий дескриптор файлу. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`filehandle`

Файловий дескриптор, у якому записати зображення.

`format`

Формат зображення. Список допустимих специфікаторів формату залежить від скомпілюваного набору функцій програми ImageMagick і може бути запитаний під час виконання за допомогою методу [Imagick::queryFormats()](imagick.queryformats.md)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::queryFormats()](imagick.queryformats.md) - Повертає формати, що підтримуються Imagick