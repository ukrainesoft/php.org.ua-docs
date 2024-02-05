---
navigation:
  - function.ibase-errmsg.md: « ibase\_errmsg
  - function.ibase-fetch-assoc.md: ibase\_fetch\_assoc »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_execute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_execute

(PHP 5, PHP 7 < 7.4.0)

ibase\_execute — Виконує попередньо підготовлений запит

### Опис

```methodsynopsis
ibase_execute(resource $query, mixed ...$values): resource
```

Виконує запит, підготовлений за допомогою [ibase\_prepare()](function.ibase-prepare.md)

Це набагато ефективніше, ніж використання [ibase\_query()](function.ibase-query.md), якщо ви повторюєте той самий тип запиту кілька разів, змінюючи лише деякі параметри.

### Список параметрів

`query`

Запит InterBase, підготовлений за допомогою [ibase\_prepare()](function.ibase-prepare.md)

`values`

### Значення, що повертаються

Якщо запит викликає помилку, повертає **`false`**. Якщо запит виконаний успішно, і є (можливо порожній) набір результатів (як у запиті SELECT), повертає ідентифікатор результату. Якщо запит виконано успішно та результатів не було, повертається **`true`**

> **Зауваження** :
> 
> Функція повертає кількість рядків, які торкнулися запиту (якщо > 0 і застосовується до типу оператора). Якщо запит виконано успішно, але не торкнувся жодного рядка (наприклад, UPDATE неіснуючого запису), поверне **`true`**

### Приклади

**Пример #1 Пример использования**ibase\_execute()\*\*\*\*

```php
<?php

$dbh = ibase_connect($host, $username, $password);

$updates = array(
    1 => 'Eric',
    5 => 'Filip',
    7 => 'Larry'
);

$query = ibase_prepare($dbh, "UPDATE FOO SET BAR = ? WHERE BAZ = ?");

foreach ($updates as $baz => $bar) {
    ibase_execute($query, $bar, $baz);
}

?>
```

### Дивіться також

-   [ibase\_query()](function.ibase-query.md) \- Виконує запит до бази даних InterBase
