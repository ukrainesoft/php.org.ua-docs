Надсилання статусу завдання (застарілий метод)

-   [« GearmanJob::setReturn](gearmanjob.setreturn.html)
    
-   [GearmanJob::unique »](gearmanjob.unique.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanJob](class.gearmanjob.html)
    
-   Надсилання статусу завдання (застарілий метод)
    

# GearmanJob::status

(PECL gearman <= 0.5.0)

GearmanJob::status — Надсилання статусу завдання (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::status(int $numerator, int $denominator): bool
```

Посилає на сервер завдань і всім клієнтам, що слухають, статус поточної роботи. За допомогою цього можна дізнатися, який відсоток завдання виконаний.

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendStatus()](gearmanjob.sendstatus.html) у версії 0.6.0 модуля Gearman.

### Список параметрів

`numerator`

Частка виконаної роботи.

`denominator`

Кількість усієї роботи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::jobStatus()](gearmanclient.jobstatus.html) - Набуття статусу виконання фонового завдання
-   [GearmanTask::taskDenominator()](gearmantask.taskdenominator.html) - отримати знаменник відсотка виконаної роботи
-   [GearmanTask::taskNumerator()](gearmantask.tasknumerator.html) - отримання чисельника відсотка виконаної роботи