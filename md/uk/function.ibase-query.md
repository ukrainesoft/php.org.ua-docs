---
navigation:
  - function.ibase-prepare.md: « ibase\_prepare
  - function.ibase-restore.md: ibase\_restore »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_query

(PHP 5, PHP 7 < 7.4.0)

ibase\_query — Виконує запит до бази даних InterBase

### Опис

```methodsynopsis
ibase_query(resource $link_identifier = ?, string $query, int $bind_args = ?): resource
```

Виконує запит до бази даних InterBase.

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`query`

Запит InterBase.

`bind_args`

### Значення, що повертаються

Якщо запит викликає помилку, повертає **`false`**. У разі успішного виконання та наявності (можливо порожнього) результуючого набору (наприклад, із запитом SELECT) повертає ідентифікатор результату. Якщо запит був успішним та результатів не було, повертає **`true`**

> **Зауваження** :
> 
> У PHP 5.0.0 і вище ця функція повертатиме кількість рядків, які торкнулися запиту, для операторів INSERT, UPDATE та DELETE. Щоб зберегти зворотну сумісність, вона повертатиме **`true`** для цих операцій, якщо запит виконано успішно без торкання будь-яких рядків.

### Помилки

Якщо ви отримаєте повідомлення про помилку на кшталт "аритметичний висновок, numeric overflow, або string truncation. Cannot transliterate character between character sets" (це відбувається, коли ви намагаєтеся використовувати будь-який символ з діакритичними знаками) при використанні цієї функції та після використання **ibase\_query()**, необхідно встановити символьне кодування (ISO8859\_1 або ваше поточне символьне кодування).

### Приклади

**Пример #1 Пример использования**ibase\_query()\*\*\*\*

```php
<?php

$host = 'localhost:/path/to/your.gdb';

$dbh = ibase_connect($host, $username, $password);
$stmt = 'SELECT * FROM tblname';

$sth = ibase_query($dbh, $stmt) or die(ibase_errmsg());

?>
```

### Дивіться також

-   [ibase\_errmsg()](function.ibase-errmsg.md) \- Повертає повідомлення про помилку
-   [ibase\_fetch\_row()](function.ibase-fetch-row.md) \- Витягує рядок із бази даних InterBase
-   [ibase\_fetch\_object()](function.ibase-fetch-object.md) \- Отримує об'єкт із бази даних InterBase
-   [ibase\_free\_result()](function.ibase-free-result.md) \- Звільняє набір результатів
