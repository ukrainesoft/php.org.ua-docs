Встановлює колір рамки зображення

-   [« Imagick::setImageBluePrimary](imagick.setimageblueprimary.html)
    
-   [Imagick::setImageChannelDepth »](imagick.setimagechanneldepth.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює колір рамки зображення
    

# Imagick::setImageBorderColor

(PECL imagick 2, PECL imagick 3)

Imagick::setImageBorderColor — Встановлює колір зображення.

### Опис

```methodsynopsis
public Imagick::setImageBorderColor(mixed $border): bool
```

Встановлює колір кадру зображення.

### Список параметрів

`border`

Колір рамки

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия             | Описание                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------|
| PECL imagick 2.1.0 | Тепер дозволяється передавати рядок, який представляє колір як параметр. Попередні версії допускають лише об'єкт ImagickPixel. |