---
navigation:
  - function.ibase-prepare.html: « ibaseprepare
  - function.ibase-restore.html: ibaserestore »
  - index.html: PHP Manual
  - ref.ibase.html: Функции Firebird/InterBase
title: ibasequery
---
# ibasequery

(PHP 5, PHP 7 < 7.4.0)

ibasequery — Виконує запит до бази даних InterBase

### Опис

```methodsynopsis
ibase_query(resource $link_identifier = ?, string $query, int $bind_args = ?): resource
```

Виконує запит до бази даних InterBase.

### Список параметрів

`link_identifier`

Ідентифікатор посилання на InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`query`

Запит InterBase.

`bind_args`

### Значення, що повертаються

Якщо запит викликає помилку, повертає **`false`**. У разі успішного виконання та наявності (можливо порожнього) результуючого набору (наприклад, із запитом SELECT) повертає ідентифікатор результату. Якщо запит був успішним та результатів не було, повертає **`true`**

> **Зауваження**
> 
> У PHP 5.0.0 і вище ця функція повертатиме кількість рядків, які торкнулися запиту, для операторів INSERT, UPDATE та DELETE. Щоб зберегти зворотну сумісність, вона повертатиме **`true`** для цих операцій, якщо запит виконано успішно без торкання будь-яких рядків.

### Помилки

Якщо ви отримаєте повідомлення про помилку на кшталт "аритметичний висновок, numeric overflow, або string truncation. Cannot transliterate character between character sets" (це відбувається, коли ви намагаєтеся використовувати будь-який символ з діакритичними знаками) при використанні цієї функції та після використання **ibasequery()**, необхідно встановити символьне кодування (ISO88591 або ваше поточне символьне кодування).

### Приклади

**Приклад #1 Приклад використання **ibasequery()****

```php
<?php

$host = 'localhost:/path/to/your.gdb';

$dbh = ibase_connect($host, $username, $password);
$stmt = 'SELECT * FROM tblname';

$sth = ibase_query($dbh, $stmt) or die(ibase_errmsg());

?>
```

### Дивіться також

-   [ibaseerrmsg()](function.ibase-errmsg.html) - Повертає повідомлення про помилку
-   [ibasefetchrow()](function.ibase-fetch-row.html) - Витягує рядок із бази даних InterBase
-   [ibasefetchobject()](function.ibase-fetch-object.html) - Отримує об'єкт із бази даних InterBase
-   [ibasefreeresult()](function.ibase-free-result.html) - Звільняє набір результатів
