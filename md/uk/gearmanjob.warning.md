---
navigation:
  - gearmanjob.unique.md: '« GearmanJob::unique'
  - gearmanjob.workload.md: 'GearmanJob::workload »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::warning'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::warning

(PECL gearman <= 0.5.0)

GearmanJob::warning — Надсилання попередження (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::warning(string $warning): bool
```

Під час виконання завдання надсилає попередження.

> **Зауваження** :
> 
> Цей метод було замінено на [GearmanJob::sendWarning()](gearmanjob.sendwarning.md) у версії 0.6.0 модуля Gearman.

### Список параметрів

`warning`

Повідомлення попередження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanJob::sendComplete()](gearmanjob.sendcomplete.md) \- Відправлення результату та статусу завершення
-   [GearmanJob::sendException()](gearmanjob.sendexception.md) \- Відправлення виключення завдання, що виконується
-   [GearmanJob::sendFail()](gearmanjob.sendfail.md) \- Відправлення статусу невдалої операції
