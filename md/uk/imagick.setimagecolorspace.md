Встановлює колірний простір зображення

-   [« Imagick::setImageColormapColor](imagick.setimagecolormapcolor.md)
    
-   [Imagick::setImageCompose »](imagick.setimagecompose.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Встановлює колірний простір зображення
    

# Imagick::setImageColorspace

(PECL imagick 2, PECL imagick 3)

Imagick::setImageColorspace — Встановлює колірний простір зображення

### Опис

```methodsynopsis
public Imagick::setImageColorspace(int $colorspace): bool
```

Встановлює колірний простір зображення. Метод слід використовувати під час створення нових зображень. Щоб змінити колірний простір існуючого зображення, потрібно використовувати [Imagick::transformImageColorspace()](imagick.transformimagecolorspace.md)

### Список параметрів

`colorspace`

Одна з [COLORSPACE констант](imagick.constants.html#imagick.constants.colorspace)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.