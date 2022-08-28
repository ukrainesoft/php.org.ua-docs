Додає нове зображення до списку зображень об'єкту Imagick

-   [« Imagick::adaptiveThresholdImage](imagick.adaptivethresholdimage.html)
    
-   [Imagick::addNoiseImage »](imagick.addnoiseimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Додає нове зображення до списку зображень об'єкту Imagick
    

# Imagick::addImage

(PECL imagick 2, PECL imagick 3)

Imagick::addImage — Додає нове зображення до списку зображень об'єкту Imagick

### Опис

```methodsynopsis
public Imagick::addImage(Imagick $source): bool
```

Додає нове зображення до об'єкта Imagick із поточного положення вихідного об'єкта. Після цієї операції переміщається позиція ітератора до кінця списку.

### Список параметрів

`source`

Початковий об'єкт Imagick

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.