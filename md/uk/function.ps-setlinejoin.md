---
navigation:
  - function.ps-setlinecap.md: « ps\_setlinecap
  - function.ps-setlinewidth.md: ps\_setlinewidth »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setlinejoin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setlinejoin

(PECL ps >= 1.1.0)

ps\_setlinejoin - Встановлює спосіб з'єднання ліній

### Опис

```methodsynopsis
ps_setlinejoin(resource $psdoc, int $type): bool
```

Встановлює спосіб з'єднання ліній.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`type`

Спосіб з'єднання ліній. Можливі значення: `PS_LINEJOIN_MITER` `PS_LINEJOIN_ROUND`или`PS_LINEJOIN_BEVEL`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_setlinecap()](function.ps-setlinecap.md) \- Встановлює зовнішній вигляд закінчення лінії
-   [ps\_setlinewidth()](function.ps-setlinewidth.md) \- Встановлює ширину лінії
-   [ps\_setmiterlimit()](function.ps-setmiterlimit.md) \- Встановлює межу скосу
