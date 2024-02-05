---
navigation:
  - function.ibase-blob-open.md: « ibase\_blob\_open
  - function.ibase-commit-ret.md: ibase\_commit\_ret »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_close

(PHP 5, PHP 7 < 7.4.0)

ibase\_close — Закриває з'єднання з базою даних InterBase

### Опис

```methodsynopsis
ibase_close(resource $connection_id = null): bool
```

Закриває посилання на базу даних InterBase, пов'язану з ідентифікатором з'єднання, отриманим за допомогою [ibase\_connect()](function.ibase-connect.md). Стандартна транзакція для посилання зафіксована, інші транзакції скасовані.

### Список параметрів

`connection_id`

Ідентифікатор посилання InterBase, отриманий за допомогою [ibase\_connect()](function.ibase-connect.md). Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_connect()](function.ibase-connect.md) \- Відкриває з'єднання з базою даних
-   [ibase\_pconnect()](function.ibase-pconnect.md) \- Відкриває постійне з'єднання з базою даних InterBase
