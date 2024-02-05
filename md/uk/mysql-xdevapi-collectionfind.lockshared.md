---
navigation:
  - mysql-xdevapi-collectionfind.lockexclusive.md: '« CollectionFind::lockExclusive'
  - mysql-xdevapi-collectionfind.offset.md: 'CollectionFind::offset »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::lockShared'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::lockShared

(No version information available, might only be in Git)

CollectionFind::lockShared — Виконує операцію з SHARED LOCK

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::lockShared(int $lock_waiting_option = ?): mysql_xdevapi\CollectionFind
```

Дозволяє розділяти документи між кількома транзакціями, які блокуються в режимі спільного доступу.

Інші сеанси можуть читати рядки, але не можуть змінювати їх, доки ваша транзакція не буде зафіксована.

Якщо один із цих рядків був змінений іншою транзакцією, яка ще не зафіксована, запит почекає завершення цієї транзакції, а потім використовує зафіксовані значення.

### Список параметрів

`lock_waiting_option`

Дополнительная опция ожидания. По умолчанию имеет значение\*\*`MYSQLX_LOCK_DEFAULT`\*\*. Допустимі значення представлені константами:

-   **`MYSQLX_LOCK_DEFAULT`**
    
-   **`MYSQLX_LOCK_NOWAIT`**
    
-   **`MYSQLX_LOCK_SKIP_LOCKED`**
    

### Значення, що повертаються

Повертає об'єкт класу CollectionFind, з яким можна буде працювати далі.

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\CollectionFind::lockShared()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$session->startTransaction();

$result = $collection
  ->find("age > 50")
  ->lockShared()
  ->execute();

// ... читаем объект в режиме совместного доступа

// Завершаем транзакцию и разблокируем документ
$session->commit();
?>
```
