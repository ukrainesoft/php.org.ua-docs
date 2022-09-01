---
navigation:
  - function.ps-closepath.html: «psclosepath
  - function.ps-curveto.html: псcurveto »
  - index.html: PHP Manual
  - ref.ps.html: Функції PS
title: псcontinuetext
---
# псcontinuetext

(PECL ps >= 1.1.0)

псcontinuetext — Продовжує текст у наступному рядку

### Опис

```methodsynopsis
ps_continue_text(resource $psdoc, string $text): bool
```

Виводить текст на один рядок нижче останнього рядка. Міжрядковий інтервал береться зі значення "leading", яке має бути встановлене за допомогою [псsetvalue()](function.ps-set-value.html). Фактичне положення тексту визначається значеннями "text" та "text", які можна запросити за допомогою функції [псgetvalue()](function.ps-get-value.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

`text`

Текст для виведення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псshow()](function.ps-show.html) - Виводить текст
-   [псshowxy()](function.ps-show-xy.html) - Виводить текст у заданій позиції
-   [псshowboxed()](function.ps-show-boxed.html) - Виводить текст у поле
