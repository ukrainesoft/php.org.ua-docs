---
navigation:
  - function.imageistruecolor.md: « imageistruecolor
  - function.imagelayereffect.md: imagelayereffect »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagejpeg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagejpeg

(PHP 4, PHP 5, PHP 7, PHP 8)

imagejpeg — Виводить зображення до браузера або пише у файл

### Опис

```methodsynopsis
imagejpeg(GdImage $image, resource|string|null $file = null, int $quality = -1): bool
```

Функция**imagejpeg()** створює файл JPEG із зображення`image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

`quality`

Необов'язковий параметр, і може набувати значення в діапазоні від 0 (низька якість, маленький розмір файлу) до 100 (висока якість, великий розмір файлу). За замовчуванням (`-1`) використовується якість IJG (близько 75).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Виведення JPEG-зображень у браузер**

```php
<?php
// Создаём пустое изображение и добавляем текст
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// Устанавливаем тип содержимого в заголовок, в данном случае image/jpeg
header('Content-Type: image/jpeg');

// Выводим изображение
imagejpeg($im);

// Освобождаем память
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Приклад виведе зображення JPEG](images/21009b70229598c6a80eef8b45bf282b-imagejpeg.jpg)

**Приклад #2 Збереження зображення JPEG у файл**

```php
<?php
// Создаём пустое изображение и добавляем текст
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// Сохраняем изображение в 'simpletext.jpg'
imagejpeg($im, 'simpletext.jpg');

// Освобождаем память
imagedestroy($im);
?>
```

**Приклад #3 Виведення JPEG-зображення з 75% якістю у браузер**

```php
<?php
// Создаём пустое изображение и добавляем текст
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// Устанавливаем тип содержимого в заголовок, в данном случае image/jpeg
header('Content-Type: image/jpeg');

// Пропускаем параметр file, используя NULL, а затем устанавливаем качество в 75%
imagejpeg($im, NULL, 75);

// Освобождаем память
imagedestroy($im);
?>
```

### Примітки

> **Зауваження** :
> 
> Якщо потрібно вивести Progressive JPEG (прогресивне представлення даних), необхідно використовувати функцію [imageinterlace()](function.imageinterlace.md)для активации соответствующего режима.

### Дивіться також

-   [imagepng()](function.imagepng.md) \- Виведення PNG зображення у браузер або файл
-   [imagegif()](function.imagegif.md) \- Виводить зображення у браузер або пише у файл
-   [imagewbmp()](function.imagewbmp.md) \- Виводить зображення у браузер або пише у файл
-   [imageinterlace()](function.imageinterlace.md) \- Увімкнення або вимкнення інтерлейсингу
-   [imagetypes()](function.imagetypes.md) \- Повертає список типів зображень, які підтримує PHP збірка
