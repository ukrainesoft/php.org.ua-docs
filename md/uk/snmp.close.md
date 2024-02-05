---
navigation:
  - class.snmp.md: « SNMP
  - snmp.construct.md: 'SNMP::\_\_construct »'
  - index.md: PHP Manual
  - class.snmp.md: SNMP
title: 'SNMP::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SNMP::close

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SNMP::close — Закриває сесію SNMP

### Опис

```methodsynopsis
public SNMP::close(): bool
```

Звільняє раніше виділений об'єкт сесії SNMP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SNMP::close()\*\*\*\*

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

-   [SNMP::\_\_construct()](snmp.construct.md) \- Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP
