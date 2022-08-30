Перевіряє, чи є зображення альфа-канал

-   [« Imagick::getImage](imagick.getimage.html)
    
-   [Imagick::getImageArtifact »](imagick.getimageartifact.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Перевіряє, чи є зображення альфа-канал
    

# Imagick::getImageAlphaChannel

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::getImageAlphaChannel — Перевіряє, чи є зображення альфа-канал

### Опис

```methodsynopsis
public Imagick::getImageAlphaChannel(): bool
```

Повертає, чи є зображення альфа-канал.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо зображення має альфа-канал і **`false`**, якщо ні, тобто. зображення RGB, а не RGBA чи CMYK, а не CMYKA.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия        | Описание                                                                     |
|---------------|------------------------------------------------------------------------------|
| imagick 3.6.0 | Тепер повертає логічне значення (bool); раніше поверталося ціле число (int). |