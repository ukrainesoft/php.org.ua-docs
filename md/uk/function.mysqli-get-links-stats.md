---
navigation:
  - function.mysqli-get-client-stats.md: « mysqli\_get\_client\_stats
  - function.mysqli-report.md: mysqli\_report »
  - index.md: PHP Manual
  - ref.mysqli.md: Синоніми та застарілі функції Mysqli
title: mysqli\_get\_links\_stats
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_get\_links\_stats

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

mysqli\_get\_links\_stats — Повертає інформацію про відкриті та закешовані з'єднання MySQL

### Опис

```methodsynopsis
mysqli_get_links_stats(): array
```

**mysqli\_get\_links\_stats()** повертає інформацію про відкриті та закешовані з'єднання MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**mysqli\_get\_links\_stats()** повертає асоціативний масив із трьох цілочисельних значень з такими ключами:

`total`

Ціле число (int), що означає загальну кількість з'єднань із будь-якими статусами.

`active_plinks`

Ціле число (int), що означає кількість активних постійних (persistent) з'єднань.

`cached_plinks`

Ціле число (int), що означає кількість неактивних постійних (persistent) з'єднань.
