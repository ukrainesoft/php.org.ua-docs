---
navigation:
  - function.ps-setcolor.md: « ps\_setcolor
  - function.ps-setflat.md: ps\_setflat »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setdash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setdash

(PECL ps >= 1.1.0)

ps\_setdash - Встановлює зовнішній вигляд пунктирної лінії

### Опис

```methodsynopsis
ps_setdash(resource $psdoc, float $on, float $off): bool
```

Встановлює довжину чорних та білих частин пунктирної лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`on`

Довжина рисочки.

`off`

Довжина проміжку між рисочками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_setpolydash()](function.ps-setpolydash.md) \- Встановлює зовнішній вигляд пунктирної лінії
