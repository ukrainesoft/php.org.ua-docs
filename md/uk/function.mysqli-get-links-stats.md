---
navigation:
  - function.mysqli-get-client-stats.html: « mysqligetclientstats
  - function.mysqli-report.html: mysqlireport »
  - index.html: PHP Manual
  - ref.mysqli.html: Синоніми та застарілі функції Mysqli
title: mysqligetlinksstats
---
# mysqligetlinksstats

(PHP 5> = 5.6.0, PHP 7, PHP 8)

mysqligetlinksstats — Повертає інформацію про відкриті та закешовані з'єднання MySQL

### Опис

```methodsynopsis
mysqli_get_links_stats(): array
```

**mysqligetlinksstats()** повертає інформацію про відкриті та закешовані з'єднання MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**mysqligetlinksstats()** повертає асоціативний масив із трьох цілочисельних значень з такими ключами:

`total`

Ціле число (int), що означає загальну кількість з'єднань із будь-якими статусами.

`active_plinks`

Ціле число (int), що означає кількість активних постійних (persistent) з'єднань.

`cached_plinks`

Ціле число (int), що означає кількість неактивних постійних (persistent) з'єднань.
