---
navigation:
  - gearmanjob.data.md: '« GearmanJob::data'
  - gearmanjob.fail.md: 'GearmanJob::fail »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::exception'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::exception

(PECL gearman <= 0.5.0)

GearmanJob::exception — Надсилання виключення (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::exception(string $exception): bool
```

Надсилає виняток, що виник під час виконання роботи.

> **Зауваження** :
> 
> Цей метод було замінено на [GearmanJob::sendException()](gearmanjob.sendexception.md) у модулі Gearman версії 0.6.0.

### Список параметрів

`exception`

Опис винятку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanJob::setReturn()](gearmanjob.setreturn.md) \- Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.md) \- Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.md) \- Відправлення попередження
