Основи використання

-   [« Примеры](hrtime.examples.html)
    
-   [HRTime\\PerformanceCounter »](class.hrtime-performancecounter.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](hrtime.examples.html)
    
-   Основи використання
    

## Основи використання

Цей приклад демонструє базове використання класу StopWatch

**Приклад #1 Вимірюємо час виконання кількох блоків коду**

```php
<?php

$c = new HRTime\StopWatch;

$c->start();
/* Замеряем время выполнения этого блока кода */
for ($i = 0; $i < 1024*1024; $i++);
$c->stop();
$elapsed0 = $c->getLastElapsedTime(HRTime\Unit::NANOSECOND);

/* Тут не замеряем*/
for ($i = 0; $i < 1024*1024; $i++);

$c->start();
/* А тут снова замеряем время выполнения этого блока кода */
for ($i = 0; $i < 1024*1024; $i++);
$c->stop();
$elapsed1 = $c->getLastElapsedTime(HRTime\Unit::NANOSECOND);

$elapsed_total = $c->getElapsedTime(HRTime\Unit::NANOSECOND);

?>
```