---
navigation:
  - mysql-xdevapi-session.construct.md: '« Session::\_\_construct'
  - mysql-xdevapi-session.dropschema.md: 'Session::dropSchema »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::createSchema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::createSchema

(No version information available, might only be in Git)

Session::createSchema — Створює нову схему

### Опис

```methodsynopsis
public mysql_xdevapi\Session::createSchema(string $schema_name): mysql_xdevapi\Schema
```

Створює нову схему.

### Список параметрів

`schema_name`

Назва схеми для створення.

### Значення, що повертаються

Об'єкт Schema у разі успішного виконання у разі виникнення помилки видає виняток.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::createSchema()\*\*\*\*

```php
<?php
$uri  = 'mysqlx://happyuser:password@127.0.0.1:33060/';
$sess = mysql_xdevapi\getSession($uri);

try {

    if ($schema = $sess->createSchema('fruit')) {
        echo "Инфо: Я создал схему с именем 'fruit'\n";
    }

} catch (Exception $e) {

   echo $e->getMessage();

}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Инфо: Я создал схему с именем 'fruit'
```
