Встановлює колірний простір зображення

-   [« Imagick::setImageColormapColor](imagick.setimagecolormapcolor.html)
    
-   [Imagick::setImageCompose »](imagick.setimagecompose.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює колірний простір зображення
    

# Imagick::setImageColorspace

(PECL imagick 2, PECL imagick 3)

Imagick::setImageColorspace — Встановлює колірний простір зображення

### Опис

```methodsynopsis
public Imagick::setImageColorspace(int $colorspace): bool
```

Встановлює колірний простір зображення. Метод слід використовувати під час створення нових зображень. Щоб змінити колірний простір існуючого зображення, потрібно використовувати [Imagick::transformImageColorspace()](imagick.transformimagecolorspace.html)

### Список параметрів

`colorspace`

Одна з [COLORSPACE констант](imagick.constants.html#imagick.constants.colorspace)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.