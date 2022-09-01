---
navigation:
  - function.ps-shading.html: «psshading
  - function.ps-show-boxed.html: псshowboxed »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псshfill
---
# псshfill

(PECL ps >= 1.3.0)

псshfill - Заповнює область затіненням

### Опис

```methodsynopsis
ps_shfill(resource $psdoc, int $shadingid): bool
```

Заповнює область затіненням, яке має бути створене раніше за допомогою [псshading()](function.ps-shading.html). Це альтернативний спосіб створення візерунка із затінення [псshadingpattern()](function.ps-shading-pattern.md) і використання візерунка як колір заливки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`shadingid`

Ідентифікатор затінення, створеного раніше за допомогою [псshading()](function.ps-shading.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псshading()](function.ps-shading.md) - Створює затінення для подальшого використання
-   [псshadingpattern()](function.ps-shading-pattern.md) - Створює візерунок на основі затінення
