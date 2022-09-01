---
navigation:
  - gearmanjob.sendexception.html: '« GearmanJob::sendException'
  - gearmanjob.sendstatus.html: 'GearmanJob::sendStatus »'
  - index.html: PHP Manual
  - class.gearmanjob.html: GearmanJob
title: 'GearmanJob::sendFail'
---
# GearmanJob::sendFail

(PECL gearman >= 0.6.0)

GearmanJob::sendFail — Надсилання статусу невдалої операції

### Опис

```methodsynopsis
public GearmanJob::sendFail(): bool
```

Посилає статус про невдалу обробку, вказуючи, що завдання завершилося невдало з відомих причин (на відміну невдалого завершення, коли викидається виняток).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendException()](gearmanjob.sendexception.html) - Відправлення виключення завдання, що виконується
-   [GearmanJob::setReturn()](gearmanjob.setreturn.html) - Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.html) - Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.html) - Відправлення попередження
