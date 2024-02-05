---
navigation:
  - function.ps-setgray.md: « ps\_setgray
  - function.ps-setlinejoin.md: ps\_setlinejoin »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setlinecap
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setlinecap

(PECL ps >= 1.1.0)

ps\_setlinecap - Встановлює зовнішній вигляд закінчення лінії

### Опис

```methodsynopsis
ps_setlinecap(resource $psdoc, int $type): bool
```

Встановлює зовнішній вигляд закінчення лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`type`

Тип закінчення лінії. Можливі значення: `PS_LINECAP_BUTT` `PS_LINECAP_ROUND`или`PS_LINECAP_SQUARED`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_setlinejoin()](function.ps-setlinejoin.md) \- Встановлює спосіб з'єднання ліній
-   [ps\_setlinewidth()](function.ps-setlinewidth.md) \- Встановлює ширину лінії
-   [ps\_setmiterlimit()](function.ps-setmiterlimit.md) \- Встановлює межу скосу
