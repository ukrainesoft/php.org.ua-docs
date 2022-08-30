Отримує ім'я схеми за промовчанням

-   [« Session::generateUUID](mysql-xdevapi-session.generateuuid.html)
    
-   [Session::getSchema »](mysql-xdevapi-session.getschema.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Отримує ім'я схеми за промовчанням
    

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

**Приклад #1 Приклад використання **mysqlxdevapiSession::getSchema()****

```php
<?php
$uri = "mysqlx://testuser:testpasswd@localhost:33160/testx?ssl-mode=disabled";
$session = mysql_xdevapi\getSession($uri);

$schema = $session->getDefaultSchema();
echo $schema;
?>
```

Результат виконання цього прикладу:

```
testx
```