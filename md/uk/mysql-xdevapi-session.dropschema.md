---
navigation:
  - mysql-xdevapi-session.createschema.md: '« Session::createSchema'
  - mysql-xdevapi-session.generateuuid.md: 'Session::generateUUID »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::dropSchema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**`true`**, якщо схема видалена, або **`false`** якщо вона не існує або не може бути видалена.

Генерируется ошибка уровня\*\*`E_WARNING`\*\*якщо схема не існує.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::dropSchema()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->dropSchema("addressbook");

$session->close();
?>
```
