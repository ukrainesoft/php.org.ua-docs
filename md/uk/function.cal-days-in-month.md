Повертає кількість днів на місяць для заданого року та календаря

-   [« Календарь](ref.calendar.html)
    
-   [cal\_from\_jd »](function.cal-from-jd.html)
    
-   [PHP Manual](index.html)
    
-   [Календарь](ref.calendar.html)
    
-   Повертає кількість днів на місяць для заданого року та календаря
    

# caldaysінmonth

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

caldaysінmonth — Повертає кількість днів на місяць для заданого року та календаря

### Опис

```methodsynopsis
cal_days_in_month(int $calendar, int $month, int $year): int
```

Ця функція повертає кількість днів на місяць `month` року `year` для заданого календаря `calendar`

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

**Приклад #1 Приклад використання **caldaysінmonth()****

```php
<?php
$number = cal_days_in_month(CAL_GREGORIAN, 8, 2003); // 31
echo "Всего {$number} дней в Августе 2003 года";
?>
```