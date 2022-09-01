---
navigation:
  - imagick.clone.md: '« Imagick::clone'
  - imagick.coalesceimages.md: 'Imagick::coalesceImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::clutImage'
---
# Imagick::clutImage

(PECL imagick 2, PECL imagick 3)

Imagick::clutImage — Замінює кольори зображення.

### Опис

```methodsynopsis
public Imagick::clutImage(Imagick $lookup_table, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Замінює кольори зображення, використовуючи таблицю відповідності. Необов'язковий другий параметр замінює кольори у вказаному каналі. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`lookup_table`

Об'єкт Imagick, що містить таблицю відповідності кольорів.

`channel`

Константа [Channeltype](imagick.constants.html#imagick.constants.channel). Якщо не вказано, то за замовчуванням заміна відбувається у всіх каналах.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Використання **Imagick::clutImage()****

Заміна кольору зображення, використовуючи таблицю відповідності.

```php
<?php
$image = new Imagick('test.jpg');
$clut = new Imagick();
$clut->newImage(1, 1, new ImagickPixel('black'));
$image->clutImage($clut);
$image->writeImage('test_out.jpg');
?>
```

### Дивіться також

-   [Imagick::adaptiveBlurImage()](imagick.adaptiveblurimage.md) - Додає адаптивний фільтр розмиття до зображення
-   [Imagick::motionBlurImage()](imagick.motionblurimage.md) - Імітує розмиття у русі
-   [Imagick::radialBlurImage()](imagick.radialblurimage.md) - Радіальне розмиття зображення
