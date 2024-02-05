---
navigation:
  - function.ps-setlinejoin.md: « ps\_setlinejoin
  - function.ps-setmiterlimit.md: ps\_setmiterlimit »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setlinewidth
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setlinewidth

(PECL ps >= 1.1.0)

ps\_setlinewidth - Встановлює ширину лінії

### Опис

```methodsynopsis
ps_setlinewidth(resource $psdoc, float $width): bool
```

Встановлює ширину лінії для наступних операцій малювання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`width`

Ширина ліній у точках.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_setlinecap()](function.ps-setlinecap.md) \- Встановлює зовнішній вигляд закінчення лінії
-   [ps\_setlinejoin()](function.ps-setlinejoin.md) \- Встановлює спосіб з'єднання ліній
-   [ps\_setmiterlimit()](function.ps-setmiterlimit.md) \- Встановлює межу скосу
