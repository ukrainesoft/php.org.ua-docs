---
navigation:
  - mysql-xdevapi-session.dropschema.md: '« Session::dropSchema'
  - mysql-xdevapi-session.getdefaultschema.md: 'Session::getDefaultSchema »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::generateUUID'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::generateUUID

(No version information available, might only be in Git)

Session::generateUUID — Отримує новий UUID

### Опис

```methodsynopsis
public mysql_xdevapi\Session::generateUUID(): string
```

Генерує універсальний унікальний ідентифікатор (UUID), згенерований відповідно до [» RFC 4122](http://www.faqs.org/rfcs/rfc4122)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

UUID; рядок завдовжки 32 символи.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Session::generateUuid()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$uuid = $session->generateUuid();

var_dump($uuid);
```

Висновок наведеного прикладу буде схожим на:

```
string(32) "484B18AC7980F8D4FE84613CDA5EE84B"
```
