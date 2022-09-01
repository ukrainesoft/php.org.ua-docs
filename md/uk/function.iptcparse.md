---
navigation:
  - function.iptcembed.html: « iptcembed
  - function.jpeg2wbmp.html: jpeg2wbmp »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: iptcparse
---
# iptcparse

(PHP 4, PHP 5, PHP 7, PHP 8)

iptcparse — Розбір двійкових даних IPTC на окремі теги

### Опис

```methodsynopsis
iptcparse(string $iptc_block): array|false
```

Розбирає [» IPTC](http://www.iptc.org/) дані окремі теги.

### Список параметрів

`iptc_block`

Двійкові дані IPTC.

### Значення, що повертаються

Повертає масив значень тегів, використовуючи мітки тегів як індекс. Повертає **`false`** у разі виникнення помилки, а також якщо дані IPTC відсутні.

### Приклади

**Приклад #1 iptcparse() використовується спільно з [getimagesize()](function.getimagesize.html)**

```php
<?php
$size = getimagesize('./test.jpg', $info);
if(isset($info['APP13']))
{
    $iptc = iptcparse($info['APP13']);
    var_dump($iptc);
}
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція не потребує бібліотеки GD.
