Замінює кольори зображення на найближчий колір із еталонного зображення

-   [« Gmagick::magnifyimage](gmagick.magnifyimage.html)
    
-   [Gmagick::medianfilterimage »](gmagick.medianfilterimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Замінює кольори зображення на найближчий колір із еталонного зображення
    

# Gmagick::mapimage

(PECL gmagick >= Unknown)

Gmagick::mapimage — Замінює кольори зображення на найближчий колір із еталонного зображення

### Опис

```methodsynopsis
public Gmagick::mapimage(gmagick $gmagick, bool $dither): Gmagick
```

Замінює кольори зображення на найближчий колір із еталонного зображення.

### Список параметрів

`gmagick`

Еталонне зображення.

`dither`

Встановіть для цього цілого числа значення, відмінне від нуля, щоб розмити зображення, що відображається.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.