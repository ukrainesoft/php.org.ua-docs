Встановлює колір тла об'єкта за промовчанням

-   [« Imagick::sepiaToneImage](imagick.sepiatoneimage.md)
    
-   [Imagick::setColorspace »](imagick.setcolorspace.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Встановлює колір тла об'єкта за промовчанням
    

# Imagick::setBackgroundColor

(PECL imagick 2, PECL imagick 3)

Imagick::setBackgroundColor — Встановлює колір тла об'єкта за промовчанням

### Опис

```methodsynopsis
public Imagick::setBackgroundColor(mixed $background): bool
```

Встановлює колір тла об'єкта за промовчанням.

### Список параметрів

`background`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия             | Описание                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| PECL imagick 2.1.0 | Тепер дозволяє використовувати рядок, що представляє колір, як параметр. Попередні версії дозволяли використовувати лише об'єкт ImagickPixel. |