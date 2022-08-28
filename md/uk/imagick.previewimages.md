Швидке визначення відповідних параметрів для обробки зображень

-   [« Imagick::posterizeImage](imagick.posterizeimage.html)
    
-   [Imagick::previousImage »](imagick.previousimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Швидке визначення відповідних параметрів для обробки зображень
    

# Imagick::previewImages

(PECL imagick 2, PECL imagick 3)

Imagick::previewImages — Швидке визначення відповідних параметрів для обробки зображень

### Опис

```methodsynopsis
public Imagick::previewImages(int $preview): bool
```

Розміщує 9 мініатюр вказаного зображення за допомогою операції обробки зображення, що застосовується з різною інтенсивністю. Це допомагає швидко визначити відповідний параметр для обробки зображення.

### Список параметрів

`preview`

Тип попереднього перегляду. Дивіться [константы типа предварительного просмотра](imagick.constants.html#imagick.constants.preview)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.