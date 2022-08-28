Записує зображення у файл

-   [« Imagick::writeImage](imagick.writeimage.html)
    
-   [Imagick::writeImages »](imagick.writeimages.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Записує зображення у файл
    

# Imagick::writeImageFile

(PECL imagick 2> = 2.3.0, PECL imagick 3)

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

Формат зображення. Список допустимих специфікаторів формату залежить від скомпілюваного набору функцій програми ImageMagick і може бути запитаний під час виконання за допомогою методу [Imagick::queryFormats()](imagick.queryformats.html)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::queryFormats()](imagick.queryformats.html) - Повертає формати, що підтримуються Imagick