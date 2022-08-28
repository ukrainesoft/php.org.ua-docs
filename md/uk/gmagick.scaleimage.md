Масштабує розмір зображення

-   [« Gmagick::rotateimage](gmagick.rotateimage.html)
    
-   [Gmagick::separateimagechannel »](gmagick.separateimagechannel.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Масштабує розмір зображення
    

# Gmagick::scaleimage

(PECL gmagick >= Unknown)

Gmagick::scaleimage — Масштабує розмір зображення

### Опис

```methodsynopsis
public Gmagick::scaleimage(int $width, int $height, bool $fit = false): Gmagick
```

Масштабування розміру зображення до заданих розмірів. Інший параметр буде розрахований, якщо як будь-який з параметрів буде переданий 0.

### Список параметрів

`width`

Кількість стовпців у масштабованому зображенні.

`height`

Кількість рядків у масштабованому зображенні.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.