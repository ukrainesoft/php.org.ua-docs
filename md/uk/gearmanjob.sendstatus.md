Надсилання статусу

-   [« GearmanJob::sendFail](gearmanjob.sendfail.md)
    
-   [GearmanJob::sendWarning »](gearmanjob.sendwarning.md)
    
-   [PHP Manual](index.md)
    
-   [GearmanJob](class.gearmanjob.md)
    
-   Надсилання статусу
    

# GearmanJob::sendStatus

(PECL gearman >= 0.6.0)

GearmanJob::sendStatus — Надсилання статусу

### Опис

```methodsynopsis
public GearmanJob::sendStatus(int $numerator, int $denominator): bool
```

Посилає на сервер завдань і всім клієнтам, що слухають, статус поточної роботи. За допомогою цього можна дізнатися, який відсоток завдання виконаний.

### Список параметрів

`numerator`

Частка виконаної роботи.

`denominator`

Кількість усієї роботи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::jobStatus()](gearmanclient.jobstatus.md) - Набуття статусу виконання фонового завдання
-   [GearmanTask::taskDenominator()](gearmantask.taskdenominator.md) - отримати знаменник відсотка виконаної роботи
-   [GearmanTask::taskNumerator()](gearmantask.tasknumerator.md) - отримання чисельника відсотка виконаної роботи