---
navigation:
  - function.imageflip.md: « imageflip
  - function.imagefontwidth.md: imagefontwidth »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagefontheight
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagefontheight

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefontheight — Отримання висоти шрифту

### Опис

```methodsynopsis
imagefontheight(GdFont|int $font): int
```

Повертає висоту пікселів символу заданого шрифту.

### Список параметрів

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.md), що повертається функцією [imageloadfont()](function.imageloadfont.md) .. .

### Значення, що повертаються

Повертає висоту у пікселах.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`font` тепер приймає як екземпляр [GdFont](class.gdfont.md), і ціле число (int); раніше приймалося лише ціле число (int). |

### Приклади

**Приклад #1 Приклад використання** imagefontheight()\*\* на вбудованих шрифтах\*\*

```php
<?php
echo 'Font height: ' . imagefontheight(4);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Font height: 16
```

**Приклад #2 Использование**imagefontheight()**вместе с[imageloadfont()](function.imageloadfont.md)**

```php
<?php
// загрузка .gdf шрифта
$font = imageloadfont('anonymous.gdf');

echo 'Высота шрифта: ' . imagefontheight($font);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Font height: 43
```

### Дивіться також

-   [imagefontwidth()](function.imagefontwidth.md) \- Отримання ширини шрифту
-   [imageloadfont()](function.imageloadfont.md) \- Завантаження шрифту
