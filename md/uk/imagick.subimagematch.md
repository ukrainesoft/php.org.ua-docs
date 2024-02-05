---
navigation:
  - imagick.stripimage.md: '« Imagick::stripImage'
  - imagick.swirlimage.md: 'Imagick::swirlImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::subImageMatch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::subImageMatch

(PECL imagick 3 >= 3.3.0)

Imagick::subImageMatch — Шукає фрагмент зображення у поточному зображенні та повертає другорядне зображення.

### Опис

```methodsynopsis
public Imagick::subImageMatch(Imagick $Imagick, array &$offset = ?, float &$similarity = ?): Imagick
```

Виконує пошук фрагмента зображення в поточному зображенні і повертає другорядне зображення, в якому точний збіг є повністю білим, а якщо жоден з пікселів не збігається чорним, інакше деяким проміжним рівнем сірого. Ви також можете передати необов'язкові параметри bestMatch та similarity. Після виклику функції similarity буде встановлено на "score" подібності між другорядним зображенням і відповідною позицією на великому зображенні, bestMatch міститиме асоціативний масив з елементами x, y, width, height, які описують збігаючу область.

### Список параметрів

`Imagick`

`offset`

`similarity`

Нове зображення, що відображає ступінь подібності кожного пікселя.

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Imagick::subImageMatch()\*\*\*\*

```php
<?php
function subImageMatch($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick2 = clone $imagick;
    $imagick2->cropimage(40, 40, 250, 110);
    $imagick2->vignetteimage(0, 1, 3, 3);

    $similarity = null;
    $bestMatch = null;
    $comparison = $imagick->subImageMatch($imagick2, $bestMatch, $similarity);

    $comparison->setImageFormat('png');
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
