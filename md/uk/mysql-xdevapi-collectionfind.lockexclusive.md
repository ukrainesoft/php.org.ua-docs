---
navigation:
  - mysql-xdevapi-collectionfind.limit.md: '« CollectionFind::limit'
  - mysql-xdevapi-collectionfind.lockshared.md: 'CollectionFind::lockShared »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::lockExclusive'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::lockExclusive

(No version information available, might only be in Git)

CollectionFind::lockExclusive — Виконує операцію з EXCLUSIVE LOCK

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::lockExclusive(int $lock_waiting_option = ?): mysql_xdevapi\CollectionFind
```

Накладає на документ виняткове блокування. Доки документ заблоковано, інші транзакції не можуть оновлювати документ, виконувати вирази `SELECT ... LOCK IN SHARE MODE` чи читати дані на окремих рівнях ізоляції транзакцій. Узгоджені читання ігнорують будь-які блокування, встановлені для записів, які існують у поданні читання.

Щоб не було проблем з конкурентним доступом, має сенс викликати цей метод спільно з методом **mysql\_xdevapi\\Collection::modify()**. Фактично, ця функція використовує блокування рядків для серіалізації доступу до рядків.

### Список параметрів

`lock_waiting_option`

Дополнительная опция ожидания. Значение по умолчанию —\*\*`MYSQLX_LOCK_DEFAULT`\*\*. Допустимі значення визначені константами:

-   **`MYSQLX_LOCK_DEFAULT`**
    
-   **`MYSQLX_LOCK_NOWAIT`**
    
-   **`MYSQLX_LOCK_SKIP_LOCKED`**
    

### Значення, що повертаються

Повертає об'єкт класу CollectionFind, з яким можна буде працювати далі.

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\CollectionFind::lockExclusive()\*\*\*\*

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
