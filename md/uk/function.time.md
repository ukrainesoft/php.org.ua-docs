---
navigation:
  - function.strtotime.md: « strtotime
  - function.timezone-abbreviations-list.md: timezone\_abbreviations\_list »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: time
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# time

(PHP 4, PHP 5, PHP 7, PHP 8)

time — Повертає поточну позначку системного часу Unix

### Опис

```methodsynopsis
time(): int
```

Повертає кількість секунд, що пройшли з початку епохи Unix (1 січня 1970 00:00:00 GMT) до теперішнього часу.

> **Зауваження** :
> 
> Мітки часу Unix не містять жодної інформації щодо локального часового поясу. Рекомендується використовувати клас [DateTimeImmutable](class.datetimeimmutable.md) для роботи з інформацією про дату та час, щоб уникнути підводних каменів, пов'язаних з мітками часу Unix.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточну позначку системного часу.

### Приклади

**Приклад #1 Приклад використання** time()\*\*\*\*

```php
<?php

echo 'Сейчас: '. time();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Сейчас: 1660338149
```

### Примітки

**Підказка**

Время начала запроса доступно в глобальной переменной[$\_SERVER\['REQUEST\_TIME'\]](reserved.variables.server.md)

### Дивіться також

-   [DateTimeImmutable](class.datetimeimmutable.md)
-   [date()](function.date.md) \- Форматує тимчасову мітку Unix
-   [microtime()](function.microtime.md) \- Повертає поточну позначку часу Unix з мікросекундами
