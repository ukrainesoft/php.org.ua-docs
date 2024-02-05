---
navigation:
  - function.cubrid-get-autocommit.md: « cubrid\_get\_autocommit
  - function.cubrid-get-class-name.md: cubrid\_get\_class\_name »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_get\_charset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_get\_charset

(PECL CUBRID >= 8.3.0)

cubrid\_get\_charset — Повертає кодування поточного з'єднання CUBRID

### Опис

```methodsynopsis
cubrid_get_charset(resource $conn_identifier): string
```

Ця функція повертає кодування поточного з'єднання CUBRID та аналогічна функції сумісності CUBRID MySQL [cubrid\_client\_encoding()](function.cubrid-client-encoding.md)

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

### Значення, що повертаються

Рядок, що містить кодування поточного з'єднання CUBRID у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_get\_charset()\*\*\*\*

```php
<?php

$con = cubrid_connect("localhost", 33000, "demodb");
if (!$con)
{
    die('Could not connect.');
}

printf("CUBRID current charset: %s\n", cubrid_get_charset($con));

?>
```

Результат виконання наведеного прикладу:

```
CUBRID current charset: iso8859-1
```

### Дивіться також

-   [cubrid\_client\_encoding()](function.cubrid-client-encoding.md) \- Повертає кодування поточного з'єднання CUBRID
