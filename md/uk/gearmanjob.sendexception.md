---
navigation:
  - gearmanjob.senddata.html: '« GearmanJob::sendData'
  - gearmanjob.sendfail.html: 'GearmanJob::sendFail »'
  - index.html: PHP Manual
  - class.gearmanjob.html: GearmanJob
title: 'GearmanJob::sendException'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::setReturn()](gearmanjob.setreturn.html) - Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.html) - Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.html) - Відправлення попередження
