Масштабує розмір зображення

-   [« Imagick::sampleImage](imagick.sampleimage.md)
    
-   [Imagick::segmentImage »](imagick.segmentimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Масштабує розмір зображення
    

# Imagick::scaleImage

(PECL imagick 2, PECL imagick 3)

Imagick::scaleImage — Масштабує розмір зображення

### Опис

```methodsynopsis
public Imagick::scaleImage(    int $cols,    int $rows,    bool $bestfit = false,    bool $legacy = false): bool
```

Масштабує зображення до розмірів. Другий параметр буде обчислено, якщо в якості будь-якого з параметрів буде передано 0.

> **Зауваження**: Поведінка параметра `bestfit` було змінено у Imagick 3.0.0. До цієї версії при зміні зображення розміром 200×150 до 400×300 жодних операцій не відбувалося. В Imagick 3.0.0 і далі зображення буде масштабовано до розмірів 400x300, оскільки це найкраще відповідає ("best fit") даним розмірам. Якщо використовується параметр `bestfit`, то ширина та висота також повинні бути визначені.

### Список параметрів

`cols`

`rows`

`bestfit`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 2.1.0 | Доданий необов'язковий параметр fit. Метод тепер підтримує пропорційне масштабування. Передайте нуль як будь-який параметр для пропорційного масштабування. |

### Приклади

**Приклад #1 Приклад використання **Imagick::scaleImage()****

```php
<?php
function scaleImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->scaleImage(150, 150, true);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```