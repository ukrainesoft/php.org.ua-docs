---
navigation:
  - gearmanjob.setreturn.md: '« GearmanJob::setReturn'
  - gearmanjob.unique.md: 'GearmanJob::unique »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::status'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::status

(PECL gearman <= 0.5.0)

GearmanJob::status — Надсилання статусу завдання (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::status(int $numerator, int $denominator): bool
```

Посилає на сервер завдань і всім клієнтам, що слухають, статус поточної роботи. З допомогою цього можна дізнатися, який відсоток завдання виконано.

> **Зауваження** :
> 
> Цей метод було замінено на [GearmanJob::sendStatus()](gearmanjob.sendstatus.md) у версії 0.6.0 модуля Gearman.

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
