---
navigation:
  - imagick.setlastiterator.md: '« Imagick::setLastIterator'
  - imagick.setpage.md: 'Imagick::setPage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setOption

(PECL imagick 2, PECL imagick 3)

Imagick::setOption — Встановлює опцію

### Опис

```methodsynopsis
public Imagick::setOption(string $key, string $value): bool
```

Зв'язує одну або кілька опцій із паличкою.

### Список параметрів

`key`

`value`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Спроба досягти розміру $extent **Imagick::setOption()****

```php
<?php
    function renderJPG($extent) {
        $imagePath = $this->control->getImagePath();
        $imagick = new \Imagick(realpath($imagePath));
        $imagick->setImageFormat('jpg');
        $imagick->setOption('jpeg:extent', $extent);
        header("Content-Type: image/jpg");
        echo $imagick->getImageBlob();
    }

?>
```

**Пример #2 Пример использования**Imagick::setOption()\*\*\*\*

```php
<?php
    function renderPNG($imagePath, $format) {

        $imagick = new \Imagick(realpath($imagePath));
        $imagick->setImageFormat('png');
        $imagick->setOption('png:format', $format);
        header("Content-Type: image/png");
        echo $imagick->getImageBlob();
    }

    //Сохранение в виде 64bit PNG.
    renderPNG($imagePath, 'png64');

?>
```

**Пример #3 Пример использования**Imagick::setOption()\*\*\*\*

```php
<?php
    function renderCustomBitDepthPNG() {
        $imagePath = $this->control->getImagePath();
        $imagick = new \Imagick(realpath($imagePath));
        $imagick->setImageFormat('png');

        $imagick->setOption('png:bit-depth', '16');
        $imagick->setOption('png:color-type', 6);
        header("Content-Type: image/png");
        $crash = true;
        if ($crash) {
            echo $imagick->getImageBlob();
        }
        else {
            $tempFilename = tempnam('./', 'imagick');
            $imagick->writeimage(realpath($tempFilename));
            echo file_get_contents($tempFilename);
        }
    }

?>
```
