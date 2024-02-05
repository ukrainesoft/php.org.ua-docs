---
navigation:
  - function.ps-closepath.md: « ps\_closepath
  - function.ps-curveto.md: ps\_curveto »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_continue\_text
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_continue\_text

(PECL ps >= 1.1.0)

ps\_continue\_text — Продовжує текст у наступному рядку

### Опис

```methodsynopsis
ps_continue_text(resource $psdoc, string $text): bool
```

Виводить текст на один рядок нижче останнього рядка. Міжрядковий інтервал береться зі значення "leading", яке має бути встановлене за допомогою [ps\_set\_value()](function.ps-set-value.md). . Фактичне положення тексту визначається значеннями "text" та "text", які можна запросити за допомогою функції [ps\_get\_value()](function.ps-get-value.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`text`

Текст для виведення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_show()](function.ps-show.md) \- Виводить текст
-   [ps\_show\_xy()](function.ps-show-xy.md) \- Виводить текст у заданій позиції
-   [ps\_show\_boxed()](function.ps-show-boxed.md) \- Виводить текст у поле
