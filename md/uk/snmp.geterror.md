---
navigation:
  - snmp.geterrno.md: '« SNMP::getErrno'
  - snmp.getnext.md: 'SNMP::getnext »'
  - index.md: PHP Manual
  - class.snmp.md: SNMP
title: 'SNMP::getError'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SNMP::getError

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SNMP::getError — Отримує останнє повідомлення про помилку

### Опис

```methodsynopsis
public SNMP::getError(): string
```

Повертає рядок помилки з останнього запиту SNMP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок, що описує помилку останнього запиту SNMP.

### Приклади

**Приклад #1 Приклад використання** SNMP::getError()\*\*\*\*

```php
<?php
$session = new SNMP(SNMP::VERSION_2c, '127.0.0.1', 'boguscommunity');
var_dump(@$session->get('.1.3.6.1.2.1.1.1.0'));
var_dump($session->getError());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
string(26) "No response from 127.0.0.1"
```

### Дивіться також

-   [SNMP::getErrno()](snmp.geterrno.md) \- Отримує код останньої помилки
