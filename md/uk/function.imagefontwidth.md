---
navigation:
  - function.imagefontheight.md: « imagefontheight
  - function.imageftbbox.md: imageftbbox »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagefontwidth
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagefontwidth

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefontwidth — Отримання ширини шрифту

### Опис

```methodsynopsis
imagefontwidth(GdFont|int $font): int
```

Повертає ширину символу шрифту.

### Список параметрів

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.md), що повертається функцією [imageloadfont()](function.imageloadfont.md) .. .

### Значення, що повертаються

Повертає ширину у пікселах

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`font` тепер приймає як екземпляр [GdFont](class.gdfont.md), і ціле число (int); раніше приймалося лише ціле число (int). |

### Приклади

**Пример #1 Использование**imagefontwidth()\*\* на вбудованих шрифтах\*\*

```php
<?php
echo 'Ширина шрифта: ' . imagefontwidth(4);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Font width: 8
```

**Пример #2 Использование**imagefontwidth()**вместе с[imageloadfont()](function.imageloadfont.md)**

```php
<?php
// загрузка .gdf шрифта
$font = imageloadfont('anonymous.gdf');

echo 'Ширина шрифта: ' . imagefontwidth($font);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Font width: 23
```

### Дивіться також

-   [imagefontheight()](function.imagefontheight.md) \- Отримання висоти шрифту
-   [imageloadfont()](function.imageloadfont.md) \- Завантаження шрифту
