---
navigation:
  - function.imagefttext.md: « imagefttext
  - function.imagegd2.md: imagegd2 »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagegammacorrect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagegammacorrect

(PHP 4, PHP 5, PHP 7, PHP 8)

imagegammacorrect — Застосування гамма корекції до GD зображення

### Опис

```methodsynopsis
imagegammacorrect(GdImage $image, float $input_gamma, float $output_gamma): bool
```

Применяет гамма коррекцию к изображению`image` згідно з заданими вхідними та вихідними налаштуваннями.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`input_gamma`

Вхідна настройка гами.

`output_gamma`

Вихідна настройка гами.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Пример использования**imagegammacorrect()\*\*\*\*

```php
<?php
// Создание изображения
$im = imagecreatefromgif('php.gif');

// Корректировка гаммы, на выходе 1.537
imagegammacorrect($im, 1.0, 1.537);

// Сохранение изображения и освобождение памяти
imagegif($im, './php_gamma_corrected.gif');
imagedestroy($im);
?>
```
