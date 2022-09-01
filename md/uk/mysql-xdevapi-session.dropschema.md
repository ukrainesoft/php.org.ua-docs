---
navigation:
  - mysql-xdevapi-session.createschema.html: '« Session::createSchema'
  - mysql-xdevapi-session.generateuuid.html: 'Session::generateUUID »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.html: mysqlxdevapiSession
title: 'Session::dropSchema'
---
# Session::dropSchema

(No version information available, might only be in Git)

Session::dropSchema — Видаляє схему

### Опис

```methodsynopsis
public mysql_xdevapi\Session::dropSchema(string $schema_name): bool
```

Видаляє схему (базу даних).

### Список параметрів

`schema_name`

Ім'я схеми видалення.

### Значення, що повертаються

**`true`**, якщо схема видалена, або **`false`** якщо вона не існує або не може бути вилучена.

Генерується помилка рівня \*\*`E_WARNING`\*\*якщо схема не існує.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::dropSchema()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->dropSchema("addressbook");

$session->close();
?>
```
