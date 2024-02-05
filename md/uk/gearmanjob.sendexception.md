---
navigation:
  - gearmanjob.senddata.md: '« GearmanJob::sendData'
  - gearmanjob.sendfail.md: 'GearmanJob::sendFail »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::sendException'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::sendException

(PECL gearman >= 0.6.0)

GearmanJob::sendException — Надсилання винятку завдання, що виконується

### Опис

```methodsynopsis
public GearmanJob::sendException(string $exception): bool
```

Надсилає виняток, що виник під час виконання роботи.

### Список параметрів

`exception`

Опис винятку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanJob::setReturn()](gearmanjob.setreturn.md) \- Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.md) \- Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.md) \- Відправлення попередження
