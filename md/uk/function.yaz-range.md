---
navigation:
  - function.yaz-present.md: « yaz\_present
  - function.yaz-record.md: yaz\_record »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_range
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_range

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_range — Визначає діапазон записів для отримання

### Опис

```methodsynopsis
yaz_range(resource $id, int $start, int $number): void
```

Визначає діапазон записів для отримання.

Функція має бути викликана перед [yaz\_search()](function.yaz-search.md) або [yaz\_present()](function.yaz-present.md)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

`start`

Визначає позицію першого запису, який потрібно отримати. Номери записів йдуть від 1 до [yaz\_hits()](function.yaz-hits.md)

`number`

Визначає діапазон записів для отримання.

### Значення, що повертаються

Функція не повертає значення після виконання.
