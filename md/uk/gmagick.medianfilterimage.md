Застосовує цифровий фільтр

-   [« Gmagick::mapimage](gmagick.mapimage.md)
    
-   [Gmagick::minifyimage »](gmagick.minifyimage.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](class.gmagick.md)
    
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

Об'єкт [Gmagick](class.gmagick.md) із застосованим медіанним фільтром.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.