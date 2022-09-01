---
navigation:
  - function.yaz-present.html: « yazpresent
  - function.yaz-record.html: yazrecord »
  - index.html: PHP Manual
  - ref.yaz.html: Функции YAZ
title: yazrange
---
# yazrange

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazrange — Визначає діапазон записів для отримання

### Опис

```methodsynopsis
yaz_range(resource $id, int $start, int $number): void
```

Визначає діапазон записів для отримання.

Функція має бути викликана перед [yazsearch()](function.yaz-search.html) або [yazpresent()](function.yaz-present.html)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yazconnect()](function.yaz-connect.html)

`start`

Визначає позицію першого запису, який потрібно отримати. Номери записів йдуть від 1 до [yazhits()](function.yaz-hits.html)

`number`

Визначає діапазон записів для отримання.

### Значення, що повертаються

Функція не повертає значення після виконання.
