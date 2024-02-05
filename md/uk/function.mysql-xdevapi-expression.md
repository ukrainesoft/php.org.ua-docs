---
navigation:
  - ref.mysql-xdevapi.md: « Функції Mysql\_xdevapi
  - function.mysql-xdevapi-getsession.md: getSession »
  - index.md: PHP Manual
  - ref.mysql-xdevapi.md: Функції Mysql\_xdevapi
title: expression
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# expression

(No version information available, might only be in Git)

expression — Зв'язує підготовлені змінні твердження як параметри

### Опис

```methodsynopsis
mysql_xdevapi\expression(string $expression): object
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`expression`

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Expression()\*\*\*\*

```php
<?php
$expression = mysql_xdevapi\Expression("[age,job]");

$res  = $coll->find("age > 30")->fields($expression)->limit(3)->execute();
$data = $res->fetchAll();

print_r($data);
?>
```

Висновок наведеного прикладу буде схожим на:

```
<?php
```
