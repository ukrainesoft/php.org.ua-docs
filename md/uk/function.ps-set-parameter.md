---
navigation:
  - function.ps-set-info.md: « ps\_set\_info
  - function.ps-set-text-pos.md: ps\_set\_text\_pos »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_set\_parameter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_set\_parameter

(PECL ps >= 1.1.0)

ps\_set\_parameter — Встановлює певні параметри

### Опис

```methodsynopsis
ps_set_parameter(resource $psdoc, string $name, string $value): bool
```

Встановлює кілька параметрів, які використовують багато функцій. Параметри визначення є строковими значеннями.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`name`

Список можливих імен дивіться [ps\_get\_parameter()](function.ps-get-parameter.md)

`value`

Значення параметра.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   **ps\_get\_parameters()**
-   [ps\_set\_value()](function.ps-set-value.md) \- Встановлює певні значення
