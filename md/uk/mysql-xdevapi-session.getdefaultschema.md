---
navigation:
  - mysql-xdevapi-session.generateuuid.md: '« Session::generateUUID'
  - mysql-xdevapi-session.getschema.md: 'Session::getSchema »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-session.md: mysql\_xdevapi\\Session
title: 'Session::getDefaultSchema'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Session::getDefaultSchema

(No version information available, might only be in Git)

Session::getDefaultSchema — Отримує назву схеми за промовчанням

### Опис

```methodsynopsis
public mysql_xdevapi\Session::getDefaultSchema(): string
```

Витягує ім'я за замовчуванням схеми, яка зазвичай встановлюється в URI з'єднання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я схеми за промовчанням, визначеною з'єднанням або \*\*`null`\*\*якщо схема не встановлена.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Session::getSchema()\*\*\*\*

```php
<?php
$uri = "mysqlx://testuser:testpasswd@localhost:33160/testx?ssl-mode=disabled";
$session = mysql_xdevapi\getSession($uri);

$schema = $session->getDefaultSchema();
echo $schema;
?>
```

Результат виконання наведеного прикладу:

```
testx
```
