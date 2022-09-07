---
navigation:
  - imagick.transverseimage.md: '« Imagick::transverseImage'
  - imagick.uniqueimagecolors.md: 'Imagick::uniqueImageColors »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::trimImage'
---
# Imagick::trimImage

(PECL imagick 2, PECL imagick 3)

Imagick::trimImage — Видаляє краї зображення

### Опис

```methodsynopsis
public Imagick::trimImage(float $fuzz): bool
```

Видаляє краї, які є кольором фону із зображенням. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`fuzz`

За замовчуванням ціль повинна точно відповідати певному кольору пікселя. Однак у багатьох випадках два кольори можуть трохи відрізнятися. Розмитий елемент зображення визначає, наскільки допустимо, щоб два кольори вважалися однаковими. Цей параметр є зміною квантового діапазону.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::trimImage()****

Обріжте зображення, а потім відобразіть у браузері.

```php
<?php
/* Создайте объект и прочитайте изображение в */
$im = new Imagick("image.jpg");

/* Обрежьте изображение. */
$im->trimImage(0);

/* Выведите изображение */
header("Content-Type: image/" . $im->getImageFormat());
echo $im;
?>
```

### Дивіться також

-   [Imagick::getQuantumDepth()](imagick.getquantumdepth.md) - Повертає величину глибини
-   [Imagick::getQuantumRange()](imagick.getquantumrange.md) - Повертає величину розміру спектру Imagick
-   [imagecropauto()](function.imagecropauto.md) - Обрізає зображення автоматично, використовуючи один із доступних режимів
