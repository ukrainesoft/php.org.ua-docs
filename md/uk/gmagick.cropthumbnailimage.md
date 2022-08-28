Створення обрізаного зменшеного зображення

-   [« Gmagick::cropimage](gmagick.cropimage.html)
    
-   [Gmagick::current »](gmagick.current.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Створення обрізаного зменшеного зображення
    

# Gmagick::cropthumbnailimage

(PECL gmagick >= Unknown)

Gmagick::cropthumbnailimage — Створення обрізаного зменшеного зображення

### Опис

```methodsynopsis
public Gmagick::cropthumbnailimage(int $width, int $height): Gmagick
```

Створює зменшене зображення фіксованого розміру, спочатку застосовуючи масштабування, а потім вирізаючи необхідну область із центру.

### Список параметрів

`width`

Ширина цільового зображення.

`height`

Висота цільового зображення.

### Значення, що повертаються

Об'єкт, що вийшов [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.