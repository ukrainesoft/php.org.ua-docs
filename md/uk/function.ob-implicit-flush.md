---
navigation:
  - function.ob-gzhandler.html: « obgzhandler
  - function.ob-list-handlers.html: проlisthandlers »
  - index.html: PHP Manual
  - ref.outcontrol.html: Функції контролю виведення
title: проimplicitflush
---
# проimplicitflush

(PHP 4, PHP 5, PHP 7, PHP 8)

проimplicitflush — Увімкнення/вимкнення неявного скидання

### Опис

```methodsynopsis
ob_implicit_flush(bool $enable = true): void
```

**проimplicitflush()** включає або вимикає неявне скидання. Неявне скидання призводить до того, що операція скидання виконується після кожного виводу, тому явні виклики функції [flush()](function.flush.md) більше не знадобляться.

### Список параметрів

`enable`

`true` для включення неявного скидання, `false` в іншому випадку.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `enable` тепер набуває логічного значення (bool); раніше приймалося ціле число (int). |

### Дивіться також

-   [flush()](function.flush.md) - Скидання системного буфера виводу
-   [проstart()](function.ob-start.md) - Включення буферизації виводу
-   [проendflush()](function.ob-end-flush.md) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
