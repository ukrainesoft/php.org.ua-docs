Встановлює розмір об'єкта Gmagick

-   [« Gmagick::setsamplingfactors](gmagick.setsamplingfactors.html)
    
-   [Gmagick::shearimage »](gmagick.shearimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Встановлює розмір об'єкта Gmagick
    

# Gmagick::setsize

(PECL gmagick >= Unknown)

Gmagick::setsize — Встановлює розмір об'єкта Gmagick

### Опис

```methodsynopsis
public Gmagick::setsize(int $columns, int $rows): Gmagick
```

Встановлює розмір об'єкта Gmagick. Встановіть його, перш ніж читати сирий формат зображення, такий як **`Gmagick::COLORSPACE_RGB`** **`Gmagick::COLORSPACE_GRAY`** або **`Gmagick::COLORSPACE_CMYK`**

### Список параметрів

`columns`

Ширина у пікселях.

`rows`

Висота у пікселях.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.