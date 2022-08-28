Встановлює роздільну здатність зображення

-   [« Imagick::setRegistry](imagick.setregistry.html)
    
-   [Imagick::setResourceLimit »](imagick.setresourcelimit.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює роздільну здатність зображення
    

# Imagick::setResolution

(PECL imagick 2, PECL imagick 3)

Imagick::setResolution — Встановлює роздільну здатність зображення

### Опис

```methodsynopsis
public Imagick::setResolution(float $x_resolution, float $y_resolution): bool
```

Встановлює роздільну здатність зображення.

### Список параметрів

`x_resolution`

Горизонтальний дозвіл.

`y_resolution`

Вертикальна роздільна здатність.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Примітки

**Imagick::setResolution()** необхідно викликати перед завантаженням або створенням зображення.

### Дивіться також

-   [Imagick::setImageResolution()](imagick.setimageresolution.html) - Встановлює роздільну здатність зображення
-   [Imagick::getImageResolution()](imagick.getimageresolution.html) - Повертає роздільну здатність зображення за X і Y