---
navigation:
  - function.cubrid-affected-rows.md: « cubrid\_affected\_rows
  - function.cubrid-close.md: cubrid\_close »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_client\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_client\_encoding

(PECL CUBRID >= 8.3.1)

cubrid\_client\_encoding — Повертає кодування поточного з'єднання CUBRID

### Опис

```methodsynopsis
cubrid_client_encoding(resource $conn_identifier = ?): string
```

Функція повертає кодування поточного з'єднання CUBRID та аналогічна функції **cubrid\_get\_encoding()**

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.md)соединение.

### Значення, що повертаються

Рядок, що містить кодування поточного з'єднання CUBRID у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_client\_encoding()\*\*\*\*

```php
<?php

$con = cubrid_connect("localhost", 33000, "demodb");
if (!$con)
{
    die('Не получилось подключиться.');
}

printf("Текущая кодировка CUBRID: %s\n", cubrid_client_encoding($con));

?>
```

Результат виконання наведеного прикладу:

```
Текущая кодировка CUBRID: iso8859-1
```

### Дивіться також

-   [cubrid\_get\_charset()](function.cubrid-get-charset.md) \- Повертає кодування поточного з'єднання CUBRID
