---
navigation:
  - mysql-xdevapi-collectionfind.lockexclusive.html: '« CollectionFind::lockExclusive'
  - mysql-xdevapi-collectionfind.offset.html: 'CollectionFind::offset »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.html: mysqlxdevapiCollectionFind
title: 'CollectionFind::lockShared'
---
# CollectionFind::lockShared

(No version information available, might only be in Git)

CollectionFind::lockShared — Виконує операцію з SHARED LOCK

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::lockShared(int $lock_waiting_option = ?): mysql_xdevapi\CollectionFind
```

Дозволяє розділяти документи між кількома транзакціями, які блокуються у режимі спільного використання.

Інші сеанси можуть читати рядки, але не можуть змінювати їх, доки ваша транзакція не буде зафіксована.

Якщо якийсь із цих рядків був змінений іншою транзакцією, яка ще не зафіксована,

ваш запит почекає завершення цієї транзакції, а потім використовує найновіші значення.

### Список параметрів

`lock_waiting_option`

Додаткова опція очікування. За замовчуванням має значення **`MYSQLX_LOCK_DEFAULT`**. Допустимі значення представлені константами:

-   **`MYSQLX_LOCK_DEFAULT`**
    
-   **`MYSQLX_LOCK_NOWAIT`**
    
-   **`MYSQLX_LOCK_SKIP_LOCKED`**
    

### Значення, що повертаються

Об'єкт CollectionFind, який можна використовувати для подальшої обробки

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionFind::lockShared()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$session->startTransaction();

$result = $collection
  ->find("age > 50")
  ->lockShared()
  ->execute();

// ... читаем объект в режиме совместного использования

// Завершаем транзакцию и разблокируем документ
$session->commit();
?>
```
