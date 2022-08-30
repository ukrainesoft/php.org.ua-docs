Повертає довжину зображення у байтах

-   [« Imagick::getImageIterations](imagick.getimageiterations.md)
    
-   [Imagick::getImageMatte »](imagick.getimagematte.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Повертає довжину зображення у байтах
    

# Imagick::getImageLength

(PECL imagick 2, PECL imagick 3)

Imagick::getImageLength — Повертає довжину зображення в байтах

### Опис

```methodsynopsis
public Imagick::getImageLength(): int
```

Повертає довжину зображення у байтах.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, що містить поточний розмір зображення.

### Приклади

**Приклад #1 Приклад використання **Imagick::getImageLength()****

Отримання довжини зображення в байтах

```php
<?php
$image = new Imagick('test.jpg');
echo $image->getImageLength() . ' байт';
?>
```