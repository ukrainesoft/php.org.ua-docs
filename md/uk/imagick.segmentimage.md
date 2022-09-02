---
navigation:
  - imagick.scaleimage.md: '« Imagick::scaleImage'
  - imagick.selectiveblurimage.md: 'Imagick::selectiveBlurImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::segmentImage'
---
# Imagick::segmentImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::segmentImage — Сегментує зображення

### Опис

```methodsynopsis
public Imagick::segmentImage(    int $COLORSPACE,    float $cluster_threshold,    float $smooth_threshold,    bool $verbose = false): bool
```

Аналізує зображення та визначає схожі об'єкти. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.5 або старшим.

### Список параметрів

`COLORSPACE`

Одна з [констант COLORSPACE](imagick.constants.md#imagick.constants.colorspace)

`cluster_threshold`

Відсоток, який описує мінімальну кількість пікселів, що містяться в гексаедрі, перш ніж він вважатиметься коректним.

`smooth_threshold`

Усуває шум на гістограмі.

`verbose`

Визначає, чи виводити детальну інформацію про розпізнані класи.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Imagick::segmentImage()****

```php
<?php
function segmentImage($imagePath, $colorSpace, $clusterThreshold, $smoothThreshold) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->segmentImage($colorSpace, $clusterThreshold, $smoothThreshold);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

segmentImage($imagePath, \Imagick::COLORSPACE_RGB, 5, 5);

?>
```
