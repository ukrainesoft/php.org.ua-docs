---
navigation:
  - function.ps-setpolydash.md: « ps\_setpolydash
  - function.ps-shading.md: ps\_shading »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_shading\_pattern
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_shading\_pattern

(PECL ps >= 1.3.0)

ps\_shading\_pattern — Створює візерунок на основі затінення

### Опис

```methodsynopsis
ps_shading_pattern(resource $psdoc, int $shadingid, string $optlist): int|false
```

Створює візерунок на основі затінення, яке має бути створене раніше за допомогою [ps\_shading()](function.ps-shading.md). Затінення шаблони можна використовувати як звичайні шаблони.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`shadingid`

Ідентифікатор затінення, раніше створеного за допомогою [ps\_shading()](function.ps-shading.md)

`optlist`

Аргумент нині не використовується.

### Значення, що повертаються

Ідентифікатор шаблону або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_shading()](function.ps-shading.md) \- Створює затінення для подальшого використання
-   [ps\_shfill()](function.ps-shfill.md) \- Заповнює область затіненням
