---
navigation:
  - mysql-xdevapi-collectionfind.limit.md: '« CollectionFind::limit'
  - mysql-xdevapi-collectionfind.lockshared.md: 'CollectionFind::lockShared »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysqlxdevapiCollectionFind
title: 'CollectionFind::lockExclusive'
---
# CollectionFind::lockExclusive

(No version information available, might only be in Git)

CollectionFind::lockExclusive — Виконує операцію з EXCLUSIVE LOCK

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::lockExclusive(int $lock_waiting_option = ?): mysql_xdevapi\CollectionFind
```

Блокує виключно документ, інші транзакції блокуються з моменту оновлення документа і доти, доки документ заблоковано. Поки документ заблоковано, інші транзакції не можуть оновлювати ці документи, виконувати SELECT ... LOCK IN SHARE MODE або читати дані на певних рівнях ізоляції транзакцій. Послідовні читання ігнорують будь-які блокування, встановлені для записів, які існують у поданні читання.

Функція корисна безпосередньо з командою modify() щоб уникнути проблем паралелізму. По суті вона серіалізує доступ до рядка через блокування рядка.

### Список параметрів

`lock_waiting_option`

Додаткова опція очікування. За замовчуванням має значення **`MYSQLX_LOCK_DEFAULT`**. Допустимі значення представлені константами:

-   **`MYSQLX_LOCK_DEFAULT`**
    
-   **`MYSQLX_LOCK_NOWAIT`**
    
-   **`MYSQLX_LOCK_SKIP_LOCKED`**
    

### Значення, що повертаються

Повертає об'єкт CollectionFind, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionFind::lockExclusive()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$session->startTransaction();

$result = $collection
  ->find("age > 50")
  ->lockExclusive()
  ->execute();

// ... выполняем операцию с объектом

// Завершаем транзакцию и разблокируем документ
$session->commit();
?>
```
