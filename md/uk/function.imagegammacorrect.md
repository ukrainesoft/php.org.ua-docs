---
navigation:
  - function.imagefttext.html: « imagefttext
  - function.imagegd2.html: imagegd2 »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagegammacorrect
---
# imagegammacorrect

(PHP 4, PHP 5, PHP 7, PHP 8)

imagegammacorrect — Застосування гамма корекції до GD зображення

### Опис

```methodsynopsis
imagegammacorrect(GdImage $image, float $input_gamma, float $output_gamma): bool
```

Застосовує гамма корекцію до зображення `image` згідно з заданими вхідними та вихідними налаштуваннями.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`input_gamma`

Вхідна настройка гами.

`output_gamma`

Вихідна настройка гами.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagegammacorrect()****

```php
<?php
// Создание изображения
$im = imagecreatefromgif('php.gif');

// Корректировка гаммы, на выходе 1.537
imagegammacorrect($im, 1.0, 1.537);

// Сохранение изображения и освобождение памяти
imagegif($im, './php_gamma_corrected.gif');
imagedestroy($im);
?>
```
