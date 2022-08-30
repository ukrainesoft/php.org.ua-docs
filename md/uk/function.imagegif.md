Виводить зображення у браузер або пише у файл

-   [« imagegetinterpolation](function.imagegetinterpolation.html)
    
-   [imagegrabscreen »](function.imagegrabscreen.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Виводить зображення у браузер або пише у файл
    

# imagegif

(PHP 4, PHP 5, PHP 7, PHP 8)

imagegif - Виводить зображення в браузер або пише у файл

### Опис

```methodsynopsis
imagegif(GdImage $image, resource|string|null $file = null): bool
```

**imagegif()** створює GIF файл `file` із зображення `image`. Аргумент `image` повертається функціями [imagecreate()](function.imagecreate.html) або `imagecreatefrom*`

Файл матиме формат GIF87a, якщо зображення не було зроблено прозорою функцією [imagecolortransparent()](function.imagecolortransparent.html). У цьому випадку формат файлу буде GIF89a.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Описание                                                                                         |
|--------|--------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Виведення зображення за допомогою **imagegif()****

```php
<?php
// Создание изображения
$im = imagecreatetruecolor(100, 100);

// Создание белого фона
imagefilledrectangle($im, 0, 0, 99, 99, 0xFFFFFF);

// Рисование текста на изображении
imagestring($im, 3, 40, 20, 'GD библиотека', 0xFFBA00);

// Вывод изображения в броузер
header('Content-Type: image/gif');

imagegif($im);
imagedestroy($im);
?>
```

**Приклад #2 Перетворення PNG на GIF, використовуючи **imagegif()****

```php
<?php

// Загрузка PNG
$png = imagecreatefrompng('./php.png');

// Сохранение как GIF
imagegif($png, './php.gif');

// Освобождение памяти
imagedestroy($png);

// готово
echo 'Преобразование PNG в GIF успешно завершено!';
?>
```

### Примітки

> **Зауваження**
> 
> Наступний приклад коду дозволить вам писати PHP-додатки, які будуть простіше портуватися на різні системи. У ньому використовується автовизначення типу GD підтримки, доступної в даний момент. Замініть рядки: `header ("Content-Type: image/gif"); imagegif ($im);` більш переносимі:
> 
> ```php
> <?php
> // Создание нового изображения
> $im = imagecreatetruecolor(100, 100);
> 
> // Какие-либо операции с изображением
> 
> // Обработка вывода
> if(function_exists('imagegif'))
> {
>     // для GIF
>     header('Content-Type: image/gif');
> 
>     imagegif($im);
> }
> elseif(function_exists('imagejpeg'))
> {
>     // для JPEG
>     header('Content-Type: image/jpeg');
> 
>     imagejpeg($im, NULL, 100);
> }
> elseif(function_exists('imagepng'))
> {
>     // для PNG
>     header('Content-Type: image/png');
> 
>     imagepng($im);
> }
> elseif(function_exists('imagewbmp'))
> {
>     // для WBMP
>     header('Content-Type: image/vnd.wap.wbmp');
> 
>     imagewbmp($im);
> }
> else
> {
>     imagedestroy($im);
> 
>     die('В этом PHP сервере нет поддержки изображений');
> }
> 
> // Если не поддерживается ни один из форматов
> // освободим память
> if($im)
> {
>     imagedestroy($im);
> }
> ?>
> ```

> **Зауваження**
> 
> Ви можете використовувати функцію [imagetypes()](function.imagetypes.html) для перевірки, які формати підтримуються:
> 
> ```php
> <?php
> if(imagetypes() & IMG_GIF)
> {
>     header('Content-Type: image/gif');
>     imagegif($im);
> }
> elseif(imagetypes() & IMG_JPG)
> {
>     /* ... и т.д. */
> }
> ?>
> ```

### Дивіться також

-   [imagepng()](function.imagepng.html) - Виведення PNG зображення у браузер або файл
-   [imagewbmp()](function.imagewbmp.html) - Виводить зображення до браузера або пише у файл
-   [imagejpeg()](function.imagejpeg.html) - Виводить зображення до браузера або пише у файл
-   [imagetypes()](function.imagetypes.html) - Повертає список типів зображень, які підтримує PHP збірка