Повертає масив, що представляє метрики шрифту

-   [« Imagick::quantizeImages](imagick.quantizeimages.html)
    
-   [Imagick::queryFonts »](imagick.queryfonts.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає масив, що представляє метрики шрифту
    

# Imagick::queryFontMetrics

(PECL imagick 2, PECL imagick 3)

Imagick::queryFontMetrics - Повертає масив, що представляє метрики шрифту

### Опис

```methodsynopsis
public Imagick::queryFontMetrics(ImagickDraw $properties, string $text, bool $multiline = ?): array
```

Повертає багатовимірний масив, що представляє метрики шрифту.

### Список параметрів

`properties`

Об'єкт ImagickDraw, що містить властивості шрифту.

`text`

Текст.

`multiline`

Багаторядковий параметр. Якщо залишити пустим, він визначається автоматично.

### Значення, що повертаються

Повертає багатовимірний масив, що представляє метрики шрифту.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::queryFontMetrics()****

Запитує метрики для тексту та виводить результати на екран.

```php
<?php
/* Создание нового объекта Imagick */
$im = new Imagick();

/* Создание нового объекта Imagick */
$draw = new ImagickDraw();

/* Установка шрифта */
$draw->setFont('/path/to/font.ttf');

/* Вывод метрики шрифта, автоматическое определение многострочного параметра */
var_dump($im->queryFontMetrics($draw, "Hello World!"));
?>
```