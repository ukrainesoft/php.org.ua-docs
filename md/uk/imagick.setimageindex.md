Встановлює позицію ітератора

-   [« Imagick::setImageGreenPrimary](imagick.setimagegreenprimary.html)
    
-   [Imagick::setImageInterlaceScheme »](imagick.setimageinterlacescheme.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює позицію ітератора
    

# Imagick::setImageIndex

(PECL imagick 2, PECL imagick 3)

Imagick::setImageIndex — Встановлює позицію ітератора

**Увага**

Функція оголошена *Застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::setImageIndex(int $index): bool
```

Встановлює ітератор у позицію списку зображень, вказану параметром index.

Цей метод оголошено застарілим. Використовуйте [Imagick::setIteratorIndex()](imagick.setiteratorindex.html)

### Список параметрів

`index`

Позиція встановлення ітератора.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.