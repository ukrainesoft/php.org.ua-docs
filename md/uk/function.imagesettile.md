Встановлення зображення, яке буде використано як елемент мозаїчної заливки

-   [« imagesetthickness](function.imagesetthickness.html)
    
-   [imagestring »](function.imagestring.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Встановлення зображення, яке буде використано як елемент мозаїчної заливки
    

# imagesettile

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagesettile — Встановлення зображення, яке буде використано як елемент мозаїчної заливки

### Опис

```methodsynopsis
imagesettile(GdImage $image, GdImage $tile): bool
```

**imagesettile()** задає зображення, яке буде використано як елемент мозаїчної заливки такими функціями, як [imagefill()](function.imagefill.html) і [imagefilledpolygon()](function.imagefilledpolygon.html) при використанні спеціального кольору **`IMG_COLOR_TILED`**

Це зображення використовується для замощення області зображення копіями. Може використовувати *будь-яке* GD зображення. А якщо встановити прозорий колір для цього зображення функцією [imagecolortransparent()](function.imagecolortransparent.html), деякі частини зображення нижче будуть просвічувати через створену мозаїку.

**Застереження**

Додаткові дії після завершення роботи з мозаїчним елементом не потрібні, проте якщо це зображення буде видалено (або дозволити PHP видалити його), не можна використовувати колір **`IMG_COLOR_TILED`** доки не буде задано нове зображення!

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`tile`

Об'єкт зображення для використання в мозаїці.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` і `tile` тепер чекають на екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesettile()****

```php
<?php
// Загрузка внешнего изображения
$zend = imagecreatefromgif('./zend.gif');

// Создание изображения 200x200
$im = imagecreatetruecolor(200, 200);

// Установка мозаичного элемента
imagesettile($im, $zend);

// Заливка
imagefilledrectangle($im, 0, 0, 199, 199, IMG_COLOR_TILED);

// Вывод картинки в броузер
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
imagedestroy($zend);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagesettile()](images/21009b70229598c6a80eef8b45bf282b-imagesettile.png)