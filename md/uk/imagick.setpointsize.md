Встановлює розмір точки

-   [« Imagick::setPage](imagick.setpage.html)
    
-   [Imagick::setProgressMonitor »](imagick.setprogressmonitor.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює розмір точки
    

# Imagick::setPointSize

(PECL imagick 2> = 2.1.0, PECL imagick 3)

Imagick::setPointSize — Встановлює розмір точки

### Опис

```methodsynopsis
public Imagick::setPointSize(float $point_size): bool
```

Встановлює об'єкт властивість розміру точки. Метод можна використовувати, наприклад, для встановлення розміру шрифту для caption: формат псевдозображень. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.7 або старшим.

### Список параметрів

`point_size`

Розмір точки.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::setPointSize()****

Приклад використання Imagick::setPointSize

```php
<?php
/* Создание нового объекта Imagick */
$im = new Imagick();

/* Установка шрифта для объекта */
$im->setFont("example.ttf");

/* Установка размера */
$im->setPointSize(12);

/* Создание заголовка */
$im->newPseudoImage(100, 100, "caption:Hello");

/* Работа с изображением */
?>
```

### Дивіться також

-   [Imagick::getPointSize()](imagick.getpointsize.html) - Повертає розмір точки