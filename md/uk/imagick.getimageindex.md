Повертає індекс поточного активного зображення

-   [« Imagick::getImageHistogram](imagick.getimagehistogram.md)
    
-   [Imagick::getImageInterlaceScheme »](imagick.getimageinterlacescheme.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Повертає індекс поточного активного зображення
    

# Imagick::getImageIndex

(PECL imagick 2, PECL imagick 3)

Imagick::getImageIndex — Повертає індекс активного поточного зображення.

**Увага**

Функція оголошена *Застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::getImageIndex(): int
```

Повертає індекс активного поточного зображення в об'єкті Imagick. Цей метод оголошено застарілим. Використовуйте [Imagick::getIteratorIndex()](imagick.getiteratorindex.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, що містить індекс зображення у стеку.

### Помилки

Викликає ImagickException у разі виникнення помилки.