---
navigation:
  - function.yaz-present.md: « yazpresent
  - function.yaz-record.md: yazrecord »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
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

Функція має бути викликана перед [yazsearch()](function.yaz-search.md) або [yazpresent()](function.yaz-present.md)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yazconnect()](function.yaz-connect.md)

`start`

Визначає позицію першого запису, який потрібно отримати. Номери записів йдуть від 1 до [yazhits()](function.yaz-hits.md)

`number`

Визначає діапазон записів для отримання.

### Значення, що повертаються

Функція не повертає значення після виконання.
