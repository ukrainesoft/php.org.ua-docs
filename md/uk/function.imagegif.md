---
navigation:
  - function.imagegetinterpolation.md: « imagegetinterpolation
  - function.imagegrabscreen.md: imagegrabscreen »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagegif
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagegif

(PHP 4, PHP 5, PHP 7, PHP 8)

imagegif - Виводить зображення в браузер або пише у файл

### Опис

```methodsynopsis
imagegif(GdImage $image, resource|string|null $file = null): bool
```

**imagegif()** створює GIF файл `file`из изображения`image`Аргумент`image` повертається функціями [imagecreate()](function.imagecreate.md)или`imagecreatefrom*`

Файл матиме формат GIF87a, якщо зображення не було зроблено прозорою функцією [imagecolortransparent()](function.imagecolortransparent.md). У цьому випадку формат файлу буде GIF89a.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Виведення зображення за допомогою **imagegif()****

```php
<?php
// Создание изображения
$im = imagecreatetruecolor(100, 100);

// Создание белого фона
imagefilledrectangle($im, 0, 0, 99, 99, 0xFFFFFF);

// Рисование текста на изображении
imagestring($im, 3, 40, 20, 'GD библиотека', 0xFFBA00);

// Вывод изображения в броузер
header('Content-Type: image/gif');

imagegif($im);
imagedestroy($im);
?>
```

**Приклад #2 Преобразование PNG в GIF, используя**imagegif()\*\*\*\*

```php
<?php

// Загрузка PNG
$png = imagecreatefrompng('./php.png');

// Сохранение как GIF
imagegif($png, './php.gif');

// Освобождение памяти
imagedestroy($png);

// готово
echo 'Преобразование PNG в GIF успешно завершено!';
?>
```

### Примітки

> **Зауваження** :
> 
> Наступний приклад коду дозволить вам писати PHP-додатки, які будуть простіше портуватися на різні системи. У ньому використовується автовизначення типу GD підтримки, доступної в даний момент. Замініть рядки: `header ("Content-Type: image/gif"); imagegif ($im);` на більш переносимі:
> 
> ```php
> <?php
> // Створення нового зображення
> $im = imagecreatetruecolor(100, 100);
> 
> // Будь-які операції із зображенням
> 
> // Обробка висновку
> if(function_exists('imagegif'))
> {
>     // для GIF
>     header('Content-Type: image/gif');
> 
>     imagegif($im);
> }
> elseif(function_exists('imagejpeg'))
> {
>     // для JPEG
>     header('Content-Type: image/jpeg');
> 
>     imagejpeg($im, NULL, 100);
> }
> elseif(function_exists('imagepng'))
> {
>     // для PNG
>     header('Content-Type: image/png');
> 
>     imagepng($im);
> }
> elseif(function_exists('imagewbmp'))
> {
>     // для WBMP
>     header('Content-Type: image/vnd.wap.wbmp');
> 
>     imagewbmp($im);
> }
> else
> {
>     imagedestroy($im);
> 
>     die('У цьому PHP сервері немає підтримки зображень');
> }
> 
> // Якщо не підтримується жоден із форматів
> // звільнимо пам'ять
> if($im)
> {
>     imagedestroy($im);
> }
> ?>
> ```

> **Зауваження** :
> 
> Ви можете використовувати функцію [imagetypes()](function.imagetypes.md) для перевірки, які формати підтримуються:
> 
> ```php
> <?php
> if(imagetypes() & IMG_GIF)
> {
>     header('Content-Type: image/gif');
>     imagegif($im);
> }
> elseif(imagetypes() & IMG_JPG)
> {
>     /* ... і т.д. */
> }
> ?>
> ```

### Дивіться також

-   [imagepng()](function.imagepng.md) \- Виведення PNG зображення у браузер або файл
-   [imagewbmp()](function.imagewbmp.md) \- Виводить зображення у браузер або пише у файл
-   [imagejpeg()](function.imagejpeg.md) \- Виводить зображення у браузер або пише у файл
-   [imagetypes()](function.imagetypes.md) \- Повертає список типів зображень, які підтримує PHP збірка
