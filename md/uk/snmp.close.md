Закриває сесію SNMP

-   [« SNMP](class.snmp.html)
    
-   [SNMP::construct »](snmp.construct.html)
    
-   [PHP Manual](index.html)
    
-   [SNMP](class.snmp.html)
    
-   Закриває сесію SNMP
    

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
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  # ...
  # получить, что-то сделать и т.д.
  # ...
  $session->close();
?>
```

### Дивіться також

-   [SNMP::construct()](snmp.construct.html) - Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP