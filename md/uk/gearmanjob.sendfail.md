---
navigation:
  - gearmanjob.sendexception.md: '« GearmanJob::sendException'
  - gearmanjob.sendstatus.md: 'GearmanJob::sendStatus »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
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

-   [GearmanJob::sendException()](gearmanjob.sendexception.md) - Відправлення виключення завдання, що виконується
-   [GearmanJob::setReturn()](gearmanjob.setreturn.md) - Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.md) - Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.md) - Відправлення попередження
