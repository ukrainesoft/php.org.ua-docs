---
navigation:
  - function.ps-show-xy2.md: « ps\_show\_xy2
  - function.ps-show2.md: ps\_show2 »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_show\_xy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_show\_xy

(PECL ps >= 1.1.0)

ps\_show\_xy — Виводить текст у заданій позиції

### Опис

```methodsynopsis
ps_show_xy(    resource $psdoc,    string $text,    float $x,    float $y): bool
```

Виводить текст у заданій текстовій позиції.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`text`

Текст для виведення.

`x`

Координата X лівого нижнього кута поля, що оточує текст.

`y`

Координата Y лівого нижнього кута поля навколишнього тексту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_continue\_text()](function.ps-continue-text.md) \- Продовжує текст у наступному рядку
-   [ps\_show()](function.ps-show.md) \- Виводить текст
