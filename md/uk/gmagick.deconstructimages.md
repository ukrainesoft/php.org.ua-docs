Повертає певні піксельні різницю між зображеннями

-   [« Gmagick::cyclecolormapimage](gmagick.cyclecolormapimage.md)
    
-   [Gmagick::despeckleimage »](gmagick.despeckleimage.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](class.gmagick.md)
    
-   Повертає певні піксельні різницю між зображеннями
    

# Gmagick::deconstructimages

(PECL gmagick >= Unknown)

Gmagick::deconstructimages — Повертає певні піксельні відмінності між зображеннями

### Опис

```methodsynopsis
public Gmagick::deconstructimages(): Gmagick
```

Порівнює кожне зображення з наступним у послідовності і повертає максимальну область, що обмежує будь-яких виявлених відмінностей пікселів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.