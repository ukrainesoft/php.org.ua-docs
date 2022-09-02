---
navigation:
  - function.ibase-errmsg.md: « ibaseerrmsg
  - function.ibase-fetch-assoc.md: ibasefetchassoc »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseexecute
---
# ibaseexecute

(PHP 5, PHP 7 < 7.4.0)

ibaseexecute — Виконує попередньо підготовлений запит

### Опис

```methodsynopsis
ibase_execute(resource $query, mixed ...$values): resource
```

Виконує запит, підготовлений за допомогою [ibaseprepare()](function.ibase-prepare.md)

Це набагато ефективніше, ніж використання [ibasequery()](function.ibase-query.md), якщо ви повторюєте той самий тип запиту кілька разів, змінюючи лише деякі параметри.

### Список параметрів

`query`

Запит InterBase, підготовлений за допомогою [ibaseprepare()](function.ibase-prepare.md)

`values`

### Значення, що повертаються

Якщо запит викликає помилку, повертає **`false`**. Якщо запит виконаний успішно, і є (можливо порожній) набір результатів (як у запиті SELECT), повертає ідентифікатор результату. Якщо запит виконано успішно та результатів не було, повертається **`true`**

> **Зауваження**
> 
> Функція повертає кількість рядків, які торкнулися запиту (якщо > 0 і застосовується до типу оператора). Якщо запит виконаний успішно, але не торкнувся жодного рядка (наприклад, UPDATE неіснуючого запису), поверне **`true`**

### Приклади

**Приклад #1 Приклад використання **ibaseexecute()****

```php
<?php

$dbh = ibase_connect($host, $username, $password);

$updates = array(
    1 => 'Eric',
    5 => 'Filip',
    7 => 'Larry'
);

$query = ibase_prepare($dbh, "UPDATE FOO SET BAR = ? WHERE BAZ = ?");

foreach ($updates as $baz => $bar) {
    ibase_execute($query, $bar, $baz);
}

?>
```

### Дивіться також

-   [ibasequery()](function.ibase-query.md) - Виконує запит до бази даних InterBase
