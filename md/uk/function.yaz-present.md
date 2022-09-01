---
navigation:
  - function.yaz-itemorder.html: « yazitemorder
  - function.yaz-range.html: yazrange »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazpresent
---
# yazpresent

(PHP 4> = 4.0.5, PECL yaz> = 0.9.0)

yazpresent — Готується до пошуку (Z39.50 є)

### Опис

```methodsynopsis
yaz_present(resource $id): bool
```

Функція готує повернення запису після успішного пошуку.

Функція [yazrange()](function.yaz-range.html) має бути викликана до цієї функції, щоб вказати діапазон записів, які потрібно витягти.

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yazconnect()](function.yaz-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
