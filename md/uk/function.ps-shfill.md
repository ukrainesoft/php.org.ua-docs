---
navigation:
  - function.ps-shading.md: « ps\_shading
  - function.ps-show-boxed.md: ps\_show\_boxed »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_shfill
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_shfill

(PECL ps >= 1.3.0)

ps\_shfill - Заповнює область затіненням

### Опис

```methodsynopsis
ps_shfill(resource $psdoc, int $shadingid): bool
```

Заповнює область затіненням, яке має бути створене раніше за допомогою [ps\_shading()](function.ps-shading.md). Це альтернативний спосіб створення візерунка із затінення [ps\_shading\_pattern()](function.ps-shading-pattern.md)и использования узора в качестве цвета заливки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`shadingid`

Ідентифікатор затінення, раніше створеного за допомогою [ps\_shading()](function.ps-shading.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_shading()](function.ps-shading.md) \- Створює затінення для подальшого використання
-   [ps\_shading\_pattern()](function.ps-shading-pattern.md) \- Створює візерунок на основі затінення
