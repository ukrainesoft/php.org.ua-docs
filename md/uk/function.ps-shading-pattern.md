---
navigation:
  - function.ps-setpolydash.html: «pssetpolydash
  - function.ps-shading.html: псshading »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псshadingpattern
---
# псshadingpattern

(PECL ps >= 1.3.0)

псshadingpattern — Створює візерунок на основі затінення

### Опис

```methodsynopsis
ps_shading_pattern(resource $psdoc, int $shadingid, string $optlist): int|false
```

Створює візерунок на основі затінення, яке має бути створене раніше за допомогою [псshading()](function.ps-shading.md). Затінення шаблони можна використовувати як звичайні шаблони.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`shadingid`

Ідентифікатор затінення, створеного раніше за допомогою [псshading()](function.ps-shading.md)

`optlist`

Аргумент нині не використовується.

### Значення, що повертаються

Ідентифікатор шаблону або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псshading()](function.ps-shading.md) - Створює затінення для подальшого використання
-   [псshfill()](function.ps-shfill.md) - Заповнює область затіненням
