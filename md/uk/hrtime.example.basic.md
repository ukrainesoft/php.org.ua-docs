- [« Приклади](hrtime.examples.md)
- [HRTime\PerformanceCounter »](class.hrtime-performancecounter.md)

- [PHP Manual](index.md)
- [Приклади](hrtime.examples.md)
- Основи використання

## Основи використання

Цей приклад демонструє базове використання класу StopWatch

**Приклад #1 Заміряємо час виконання кількох блоків коду**

` <?php$c = new HRTime\StopWatch;$c->start();/* Заміряємо час виконання цього блоку кода */for ($i = 0; $i < 1024*102;; ->stop();$elapsed0 = $c->getLastElapsedTime(HRTime\Unit::NANOSECOND);/* Тут не вимірюємо*/for ($i = 0; $i < 1024*1024; $i++) ->start();/* А тут знову вимірюємо час виконання цього блоку кода */for ($i = 0; $i < 1024*1024; $i++);$c->stop(); ->getLastElapsedTime(HRTime\Unit::NANOSECOND);$elapsed_total = $c->getElapsedTime(HRTime\Unit::NANOSECOND);?> `
