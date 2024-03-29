---
navigation:
  - snmp.get.md: '« SNMP::get'
  - snmp.geterror.md: 'SNMP::getError »'
  - index.md: PHP Manual
  - class.snmp.md: SNMP
title: 'SNMP::getErrno'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SNMP::getErrno

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SNMP::getErrno — Отримує код останньої помилки

### Опис

```methodsynopsis
public SNMP::getErrno(): int
```

Повернення коду помилки з останнього запиту SNMP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає одне із значень коду помилки SNMP, описаних у розділі про константи.

### Приклади

**Приклад #1 Приклад використання** SNMP::getErrno()\*\*\*\*

```php
<?php
$session = new SNMP(SNMP::VERSION_2c, '127.0.0.1', 'boguscommunity');
var_dump(@$session->get('.1.3.6.1.2.1.1.1.0'));
var_dump($session->getErrno() == SNMP::ERRNO_TIMEOUT);
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [SNMP::getError()](snmp.geterror.md) \- Отримує останнє повідомлення про помилку
