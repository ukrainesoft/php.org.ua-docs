---
navigation:
  - gearmanjob.sendfail.md: '« GearmanJob::sendFail'
  - gearmanjob.sendwarning.md: 'GearmanJob::sendWarning »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::sendStatus'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::sendStatus

(PECL gearman >= 0.6.0)

GearmanJob::sendStatus — Надсилання статусу

### Опис

```methodsynopsis
public GearmanJob::sendStatus(int $numerator, int $denominator): bool
```

Посилає на сервер завдань і всім клієнтам, що слухають, статус поточної роботи. З допомогою цього можна дізнатися, який відсоток завдання виконано.

### Список параметрів

`numerator`

Частка виконаної роботи.

`denominator`

Кількість усієї роботи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::jobStatus()](gearmanclient.jobstatus.md) \- Набуття статусу виконання фонового завдання
-   [GearmanTask::taskDenominator()](gearmantask.taskdenominator.md) \- отримати знаменник відсотка виконаної роботи
-   [GearmanTask::taskNumerator()](gearmantask.tasknumerator.md) \- отримання чисельника відсотка виконаної роботи
