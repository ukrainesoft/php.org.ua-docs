---
navigation:
  - imagick.edgeimage.md: '« Imagick::edgeImage'
  - imagick.encipherimage.md: 'Imagick::encipherImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::embossImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::embossImage

(PECL imagick 2, PECL imagick 3)

Imagick::embossImage — Повертає зображення у градаціях сірого з тривимірним ефектом

### Опис

```methodsynopsis
public Imagick::embossImage(float $radius, float $sigma): bool
```

Повертає зображення у градаціях сірого із тривимірним ефектом. Ми згортаємо зображення за допомогою гаусівського оператора заданого радіусу та стандартного відхилення (сигма). Для отримання розумних результатів радіус має бути більшим за сигму. Використовуйте радіус 0, і його буде обрано автоматично.

### Список параметрів

`radius`

Радіус ефекту

`sigma`

Сигма ефекту

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::embossImage()\*\*\*\*

```php
<?php
function embossImage($imagePath, $radius, $sigma) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->embossImage($radius, $sigma);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
