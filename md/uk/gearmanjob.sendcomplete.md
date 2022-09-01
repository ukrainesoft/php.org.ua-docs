---
navigation:
  - gearmanjob.returncode.md: '« GearmanJob::returnCode'
  - gearmanjob.senddata.md: 'GearmanJob::sendData »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::sendComplete'
---
# GearmanJob::sendComplete

(PECL gearman >= 0.6.0)

GearmanJob::sendComplete — Надсилання результату та статусу завершення

### Опис

```methodsynopsis
public GearmanJob::sendComplete(string $result): bool
```

Надсилає результати роботи клієнту та оновлює статус об'єкта на завершений.

### Список параметрів

`result`

Серіалізовані результати роботи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendFail()](gearmanjob.sendfail.md) - Відправлення статусу невдалої операції
-   [GearmanJob::setReturn()](gearmanjob.setreturn.md) - Встановлення значення, що повертається
