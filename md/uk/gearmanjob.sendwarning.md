---
navigation:
  - gearmanjob.sendstatus.md: '« GearmanJob::sendStatus'
  - gearmanjob.setreturn.md: 'GearmanJob::setReturn »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::sendWarning'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::sendWarning

(PECL gearman >= 0.6.0)

GearmanJob::sendWarning — Надсилання попередження

### Опис

```methodsynopsis
public GearmanJob::sendWarning(string $warning): bool
```

Під час виконання роботи надсилає попередження.

### Список параметрів

`warning`

Повідомлення попередження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanJob::sendComplete()](gearmanjob.sendcomplete.md) \- Відправлення результату та статусу завершення
-   [GearmanJob::sendException()](gearmanjob.sendexception.md) \- Відправлення виключення завдання, що виконується
-   [GearmanJob::sendFail()](gearmanjob.sendfail.md) \- Відправлення статусу невдалої операції
