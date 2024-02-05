---
navigation:
  - ref.calendar.md: « Календар
  - function.cal-from-jd.md: cal\_from\_jd »
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: cal\_days\_in\_month
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cal\_days\_in\_month

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

cal\_days\_in\_month — Повертає кількість днів на місяць для заданого року та календаря

### Опис

```methodsynopsis
cal_days_in_month(int $calendar, int $month, int $year): int
```

Ця функція повертає кількість днів на місяць `month`года`year`для заданного календаря`calendar`

### Список параметрів

`calendar`

Календар для обчислення

`month`

Місяць у вибраному календарі

`year`

Рік у вибраному календарі

### Значення, що повертаються

Кількість днів у конкретному місяці вибраного календаря

### Приклади

**Пример #1 Пример использования**cal\_days\_in\_month()\*\*\*\*

```php
<?php
$number = cal_days_in_month(CAL_GREGORIAN, 8, 2003); // 31
echo "Всего {$number} дней в Августе 2003 года";
?>
```
