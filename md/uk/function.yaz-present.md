---
navigation:
  - function.yaz-itemorder.md: « yaz\_itemorder
  - function.yaz-range.md: yaz\_range »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_present
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_present

(PHP 4 >= 4.0.5, PECL yaz >= 0.9.0)

yaz\_present — Готується до пошуку (Z39.50 є)

### Опис

```methodsynopsis
yaz_present(resource $id): bool
```

Функція готує повернення запису після успішного пошуку.

Функция[yaz\_range()](function.yaz-range.md) має бути викликана до цієї функції, щоб вказати діапазон записів, які потрібно витягти.

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
