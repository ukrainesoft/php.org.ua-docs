---
navigation:
  - imagick.getsamplingfactors.md: '« Imagick::getSamplingFactors'
  - imagick.getsizeoffset.md: 'Imagick::getSizeOffset »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getSize'
---
# Imagick::getSize

(PECL imagick 2, PECL imagick 3)

Imagick::getSize — Повертає розмір, пов'язаний із об'єктом Imagick

### Опис

```methodsynopsis
public Imagick::getSize(): array
```

Отримує розмір пікселів об'єкта Imagick, попередньо заданий за допомогою функції [Imagick::setSize()](imagick.setsize.md)

> **Зауваження**
> 
> Цей метод лише повертає розмір, встановлений [Imagick::setSize()](imagick.setsize.md). Якщо потрібно отримати реальні розміри зображення, використовуйте функції [Imagick::getImageWidth()](imagick.getimagewidth.md) і [Imagick::getImageHeight()](imagick.getimageheight.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає розмір, пов'язаний з об'єктом Imagick у вигляді масиву з ключами "columns" (стовпці) та "rows" (рядки).

### Приклади

**Приклад #1 Отримання розміру вихідного зображення RGB, встановлених у 200x400, після масштабування до 400x800**

```php
<?php
//Устанавливаем размер и загружаем изображение
$img = new Imagick();
$img->setSize(200, 400);
$img->readImage("image.rgb");

$img->scaleImage(400, 800);

$size = $img->getSize();
print_r($size);

echo $img->getImageWidth()."x".$img->getImageHeight();
?>
```

Результат виконання цього прикладу:

```
Array
(
    [columns] => 200
    [rows] => 400
)
400x800
```
