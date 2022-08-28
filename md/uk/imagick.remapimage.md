Перезначає кольори зображення

-   [« Imagick::reduceNoiseImage](imagick.reducenoiseimage.html)
    
-   [Imagick::removeImage »](imagick.removeimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Перезначає кольори зображення
    

# Imagick::remapImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::remapImage — Визначає кольори зображення.

### Опис

```methodsynopsis
public Imagick::remapImage(Imagick $replacement, int $DITHER): bool
```

Замінює кольори зображення на ті, які визначені параметром `replacement`. Кольори замінюються найближчим із можливих. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.5 або старшим.

### Список параметрів

`replacement`

Об'єкт Imagick, що містить кольори, що замінюють.

`DITHER`

Зверніться до списку [констант DITHERMETHOD](imagick.constants.html#imagick.constants.dithermethod)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.