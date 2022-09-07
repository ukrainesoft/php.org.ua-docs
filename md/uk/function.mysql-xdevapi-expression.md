---
navigation:
  - ref.mysql-xdevapi.md: « Функції Mysqlxdevapi
  - function.mysql-xdevapi-getsession.md: getSession »
  - index.md: PHP Manual
  - ref.mysql-xdevapi.md: Функції Mysqlxdevapi
title: expression
---
# expression

(No version information available, might only be in Git)

expression — Зв'язує підготовлені змінні твердження як параметри

### Опис

```methodsynopsis
mysql_xdevapi\expression(string $expression): object
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`expression`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiExpression()****

```php
<?php
$expression = mysql_xdevapi\Expression("[age,job]");

$res  = $coll->find("age > 30")->fields($expression)->limit(3)->execute();
$data = $res->fetchAll();

print_r($data);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
<?php
```
