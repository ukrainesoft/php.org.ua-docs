Застосовує цифровий фільтр

-   [« Gmagick::mapimage](gmagick.mapimage.html)
    
-   [Gmagick::minifyimage »](gmagick.minifyimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Застосовує цифровий фільтр
    

# Gmagick::medianfilterimage

(PECL gmagick >= Unknown)

Gmagick::medianfilterimage — Застосовує цифровий фільтр

### Опис

```methodsynopsis
public Gmagick::medianfilterimage(float $radius): void
```

Застосовує цифровий фільтр, який покращує якість зашумленого зображення. Кожен піксель замінюється медіаною у наборі сусідніх пікселів, що визначаються радіусом.

### Список параметрів

`radius`

Радіус околиці пікселів.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) із застосованим медіанним фільтром.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.