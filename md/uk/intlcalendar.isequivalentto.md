Визначає, чи дорівнює інший календар, але для іншого часу

-   [« IntlCalendar::inDaylightTime](intlcalendar.indaylighttime.html)
    
-   [IntlCalendar::isLenient »](intlcalendar.islenient.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Визначає, чи дорівнює інший календар, але для іншого часу
    

# IntlCalendar::isEquivalentTo

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::isEquivalentTo — Визначає, чи дорівнює інший календар, але для іншого часу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::isEquivalentTo(IntlCalendar $other): bool
```

Процедурний стиль

```methodsynopsis
intlcal_is_equivalent_to(IntlCalendar $calendar, IntlCalendar $other): bool
```

Повертає, чи дорівнює цей та даний об'єкт для всіх цілей, крім встановленого часу. Мовні стандарти можуть не збігатися, якщо через таку невідповідність немає жодних змін у поведінці. Сюди входить [часовой пояс](intlcalendar.gettimezone.html), чи встановлено [мягкий режим](intlcalendar.islenient.html) [повторяющиеся](intlcalendar.getrepeatedwalltimeoption.html) і [пропущені](intlcalendar.getskippedwalltimeoption.html) налаштування часу процесора, [дні тижня, коли вихідні починаються та закінчуються](intlcalendar.getdayofweektype.html) і [время, когда происходят такие переходы](intlcalendar.getweekendtransition.html). Також може містити інші параметри, специфічні для календаря, наприклад, момент переходу між григоріанським та юліанським календарем.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`other`

Інший календар, з яким буде проводитись порівняння.

### Значення, що повертаються

За відсутності помилок аргумент повертає **`true`**, якщо календарі рівні, за винятком можливо встановленого часу.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::isEquivalentTo()****

```php
<?php
$cal1 = IntlCalendar::createInstance('Europe/Lisbon', 'pt_PT');
$cal2 = IntlCalendar::createInstance('Europe/Lisbon', 'es_ES');
$cal2->clear();

var_dump($cal1->isEquivalentTo($cal2)); // true

$cal3 = IntlCalendar::createInstance('Europe/Lisbon', 'en_US');
var_dump($cal1->isEquivalentTo($cal3)); // false
var_dump($cal1->getFirstDayOfWeek(),    // 2 (Понедельник)
$cal3->getFirstDayOfWeek());            // 1 (Воскресенье)
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
int(2)
int(1)
```

### Дивіться також

-   [IntlCalendar::equals()](intlcalendar.equals.html) - Порівнює час двох об'єктів IntlCalendar щодо рівності