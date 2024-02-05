---
navigation:
  - ref.snmp.md: « Функції SNMP
  - function.snmp-get-valueretrieval.md: snmp\_get\_valueretrieval »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp\_get\_quick\_print
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp\_get\_quick\_print

(PHP 4, PHP 5, PHP 7, PHP 8)

snmp\_get\_quick\_print — Отримує поточне значення quick\_print бібліотеки NET-SNMP

### Опис

```methodsynopsis
snmp_get_quick_print(): bool
```

Повертає поточне значення, що зберігається в бібліотеці NET-SNMP для quick\_print. quick\_print за замовчуванням вимкнено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо quick\_print включений або **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**snmp\_get\_quick\_print()\*\*\*\*

```php
<?php
$quickprint = snmp_get_quick_print();
?>
```

### Дивіться також

-   [snmp\_set\_quick\_print()](function.snmp-set-quick-print.md) \- Встановлює значення enable у бібліотеці NET-SNMP для повного опису того, що робить quick\_print.
