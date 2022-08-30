Встановлює фактори вибірки зображення

-   [« Gmagick::setimagewhitepoint](gmagick.setimagewhitepoint.md)
    
-   [Gmagick::setsize »](gmagick.setsize.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](class.gmagick.md)
    
-   Встановлює фактори вибірки зображення
    

# Gmagick::setsamplingfactors

(PECL gmagick >= Unknown)

Gmagick::setsamplingfactors — Встановлює фактори вибірки зображення

### Опис

```methodsynopsis
public Gmagick::setsamplingfactors(array $factors): Gmagick
```

Встановлює фактори вибірки зображення.

### Список параметрів

`factors`

Масив значень типу double, що представляє фактор вибірки кожного компонента кольору (у порядку RGB).

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.