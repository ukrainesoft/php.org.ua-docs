Додає випадковий шум до зображення

-   [« Gmagick::addimage](gmagick.addimage.md)
    
-   [Gmagick::annotateimage »](gmagick.annotateimage.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](class.gmagick.md)
    
-   Додає випадковий шум до зображення
    

# Gmagick::addnoiseimage

(PECL gmagick >= Unknown)

Gmagick::addnoiseimage — Додає випадковий шум до зображення

### Опис

```methodsynopsis
public Gmagick::addnoiseimage(int $noise_type): Gmagick
```

Додає випадковий шум зображення.

### Список параметрів

`noise_type`

Тип шуму. Дивіться список [констант типа шума](gmagick.constants.html#gmagick.constants.noise)

### Значення, що повертаються

Об'єкт Gmagick із доданим шумом.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.