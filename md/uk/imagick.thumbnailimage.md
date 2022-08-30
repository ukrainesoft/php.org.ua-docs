Змінює розмір зображення

-   [« Imagick::thresholdImage](imagick.thresholdimage.html)
    
-   [Imagick::tintImage »](imagick.tintimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Змінює розмір зображення
    

# Imagick::thumbnailImage

(PECL imagick 2, PECL imagick 3)

Imagick::thumbnailImage — Змінює розмір зображення

### Опис

```methodsynopsis
public Imagick::thumbnailImage(    int $columns,    int $rows,    bool $bestfit = false,    bool $fill = false,    bool $legacy = false): bool
```

Змінює розмір зображення до заданих розмірів та видаляє всі пов'язані профілі. Мета полягає в тому, щоб створювати мініатюри зображень, які підходять для відображення в Інтернеті. Якщо в якості третього параметра встановлено значення \*\*`true`\*\*тоді параметри стовпців і рядків використовуються як максимальні для кожної сторони. Обидві сторони будуть зменшені до тих пір, поки вони не стануть рівними або меншими, ніж параметр, вказаний для сторони.

> **Зауваження**: Поведінка параметра `bestfit` було змінено у Imagick 3.0.0. До цієї версії при зміні зображення розміром 200×150 до 400×300 жодних операцій не відбувалося. В Imagick 3.0.0 і далі зображення буде масштабовано до розмірів 400x300, оскільки це найкраще відповідає ("best fit") даним розмірам. Якщо використовується параметр `bestfit`, то ширина та висота також повинні бути визначені.

### Список параметрів

`columns`

Ширина зображення.

`rows`

Висота зображення.

`bestfit`

Визначає, чи примусово встановлювати максимальні значення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::thumbnailImage()****

```php
<?php
function thumbnailImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setbackgroundcolor('rgb(64, 64, 64)');
    $imagick->thumbnailImage(100, 100, true, true);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```