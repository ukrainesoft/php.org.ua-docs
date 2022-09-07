---
navigation:
  - class.snmp.md: « SNMP
  - snmp.construct.md: 'SNMP::construct »'
  - index.md: PHP Manual
  - class.snmp.md: SNMP
title: 'SNMP::close'
---
# SNMP::close

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SNMP::close — Закриває сесію SNMP

### Опис

```methodsynopsis
public SNMP::close(): bool
```

Звільняє раніше виділений об'єкт сесії SNMP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SNMP::close()****

```php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  # ...
  # получить, что-то сделать и т.д.
  # ...
  $session->close();
?>
```

### Дивіться також

-   [SNMP::construct()](snmp.construct.md) - Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP
