Встановлює позицію ітератора

-   [« Imagick::setInterlaceScheme](imagick.setinterlacescheme.html)
    
-   [Imagick::setLastIterator »](imagick.setlastiterator.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює позицію ітератора
    

# Imagick::setIteratorIndex

(PECL imagick 2, PECL imagick 3)

Imagick::setIteratorIndex — Встановлює позицію ітератора

### Опис

```methodsynopsis
public Imagick::setIteratorIndex(int $index): bool
```

Встановлює ітератор у позицію списку зображень, вказану за допомогою параметра index. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`index`

Позиція встановлення ітератора.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::setIteratorIndex()****

Створення зображення, встановлення та отримання індексу ітератора

```php
<?php
$im = new Imagick();
$im->newImage(100, 100, new ImagickPixel("red"));
$im->newImage(100, 100, new ImagickPixel("green"));
$im->newImage(100, 100, new ImagickPixel("blue"));

$im->setIteratorIndex(1);
echo $im->getIteratorIndex();
?>
```

### Дивіться також

-   [Imagick::getIteratorIndex()](imagick.getiteratorindex.html) - Повертає індекс поточного активного зображення
-   [Imagick::getImageIndex()](imagick.getimageindex.html) - Повертає індекс поточного активного зображення
-   [Imagick::setImageIndex()](imagick.setimageindex.html) - встановлює позицію ітератора