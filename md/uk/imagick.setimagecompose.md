Встановлює оператор складеного зображення

-   [« Imagick::setImageColorspace](imagick.setimagecolorspace.html)
    
-   [Imagick::setImageCompression »](imagick.setimagecompression.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює оператор складеного зображення
    

# Imagick::setImageCompose

(PECL imagick 2, PECL imagick 3)

Imagick::setImageCompose — Встановлює оператор складеного зображення

### Опис

```methodsynopsis
public Imagick::setImageCompose(int $compose): bool
```

Встановлює оператор складеного зображення, корисний для вказівки, як складати ескіз зображення під час використання методу Imagick::montageImage().

### Список параметрів

`compose`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.