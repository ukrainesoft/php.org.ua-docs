Арифметика дати/часу

-   [« Приклади](datetime.examples.html)
    
-   [DateTime »](class.datetime.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](datetime.examples.html)
    
-   Арифметика дати/часу
    

## Арифметика дати/часу

У наступних прикладах показуються деякі підводні камені обчислень дати/часу, щодо переходів на літній та зимовий час (DST), та місяців, що мають різну кількість днів.

**Приклад #1 DateTimeImmutable::add/sub додає інтервали, що охоплюють час, що минув.**

Додавання PT24H через перехід DST призведе до додавання 23/25 годин (для більшості часових поясів).

```php
<?php
$dt = new DateTimeImmutable("2015-11-01 00:00:00", new DateTimeZone("America/New_York"));
echo "Начало: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt = $dt->add(new DateInterval("PT3H"));
echo "Конец:  ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
Начало: 2015-11-01 00:00:00 -04:00
Конец:  2015-11-01 02:00:00 -05:00
```

**Приклад #2 DateTimeImmutable::modify та strtotime збільшить або зменшить значення індивідуальних компонентів**

Додавання +24 годин через перехід DST додасть точно 24 години (замість обліку переходу на зимовий або літній час).

```php
<?php
$dt = new DateTimeImmutable("2015-11-01 00:00:00", new DateTimeZone("America/New_York"));
echo "Начало: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt = $dt->modify("+24 hours");
echo "Конец:  ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
Начало:  2015-11-01 00:00:00 -04:00
Конец:   2015-11-02 00:00:00 -05:00
```

**Приклад #3 Додавання або віднімання часу може зменшити або збільшити дату**

Наприклад, 31 січня + 1 місяць поверне 2 березня (високосний рік) чи 3 березня (звичайний рік).

```php
<?php
echo "Обычный год:\n"; // В феврале 28 дней
$dt = new DateTimeImmutable("2015-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Начало: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt = $dt->modify("+1 month");
echo "Конец:  ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;

echo "Високосный год:\n"; // В феврале 29 дней
$dt = new DateTimeImmutable("2016-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Начало: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt = $dt->modify("+1 month");
echo "Конец:  ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
Обычный год:
Начало: 2015-01-31 00:00:00 -05:00
Конец:  2015-03-03 00:00:00 -05:00
Високосный год:
Начало: 2016-01-31 00:00:00 -05:00
Конец:  2016-03-02 00:00:00 -05:00
```

Для отримання останнього дня наступного місяця (тобто щоб запобігти переповненню) існує директива `last day of`

```php
<?php
echo "Обычный год:\n"; // Февраль содержит 28 дней
$dt = new DateTimeImmutable("2015-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Начало: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt = $dt->modify("last day of next month");
echo "Конец:  ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;

echo "Високосный год:\n"; // Февраль содержит 29 дней
$dt = new DateTimeImmutable("2016-01-31 00:00:00", new DateTimeZone("America/New_York"));
echo "Начало: ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
$dt = $dt->modify("last day of next month");
echo "Конец:  ", $dt->format("Y-m-d H:i:s P"), PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
Обычный год:
Начало: 2015-01-31 00:00:00 -05:00
Конец:  2015-02-28 00:00:00 -05:00
Високосный год:
Начало: 2016-01-31 00:00:00 -05:00
Конец:  2016-02-29 00:00:00 -05:00
```