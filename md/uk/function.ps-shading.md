---
navigation:
  - function.ps-shading-pattern.md: « ps\_shading\_pattern
  - function.ps-shfill.md: ps\_shfill »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_shading
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_shading

(PECL ps >= 1.3.0)

ps\_shading — Створює затінення для подальшого використання

### Опис

```methodsynopsis
ps_shading(    resource $psdoc,    string $type,    float $x0,    float $y0,    float $x1,    float $y1,    float $c1,    float $c2,    float $c3,    float $c4,    string $optlist): int|false
```

Створює затінення, яке можна використовувати функцією [ps\_shfill()](function.ps-shfill.md) або [ps\_shading\_pattern()](function.ps-shading-pattern.md)

Колір затінення може бути в будь-якому колірному просторі, крім `pattern`

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`type`

Тип затінення може бути `radial`или`axial`. Кожне затінення починається з поточного кольору заливки та закінчується заданими значеннями кольору, переданими у параметрах від `c1`до`c4`(описание их значений смотрите в[ps\_setcolor()](function.ps-setcolor.md)

`x0, x1, y0, y1`

Координати `x0` `y0` `x1` `y1` - це початкова та кінцева точки затінення. Якщо тип затінення - `radial`, дві точки є середніми точками початкового та кінцевого кіл.

`c1, c2, c3, c4`

Смотрите описание их значений в[ps\_setcolor()](function.ps-setcolor.md)

`optlist`

Якщо тип затінення `radial` `optlist` також має містити параметри `r0`и`r1` з радіусом початкового та кінцевого кола.

### Значення, що повертаються

Повертає ідентифікатор шаблону або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_shading\_pattern()](function.ps-shading-pattern.md) \- Створює візерунок на основі затінення
-   [ps\_shfill()](function.ps-shfill.md) \- Заповнює область затіненням
