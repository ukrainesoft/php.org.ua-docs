Отримує основні атрибути зображення

-   [« Imagick::paintTransparentImage](imagick.painttransparentimage.html)
    
-   [Imagick::pingImageBlob »](imagick.pingimageblob.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Отримує основні атрибути зображення
    

# Imagick::pingImage

(PECL imagick 2, PECL imagick 3)

Imagick::pingImage — Отримує основні атрибути зображення

### Опис

```methodsynopsis
public Imagick::pingImage(string $filename): bool
```

Метод можна використовувати для запиту ширини, висоти, розміру та формату зображення без зчитування всього зображення на згадку.

### Список параметрів

`filename`

Ім'я файлу, з якого потрібно прочитати інформацію.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**