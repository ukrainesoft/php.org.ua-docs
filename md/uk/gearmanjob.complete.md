---
navigation:
  - class.gearmanjob.md: « GearmanJob
  - gearmanjob.construct.md: 'GearmanJob::construct »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::complete'
---
# GearmanJob::complete

(PECL gearman <= 0.5.0)

GearmanJob::complete — Надсилання результату та статусу завершення (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::complete(string $result): bool
```

Надсилає результати обробки клієнту та оновлює статус роботи на завершений.

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendComplete()](gearmanjob.sendcomplete.md) у випуску модуля Gearman 0.6.0.

### Список параметрів

`result`

Серіалізовані результати опрацювання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendFail()](gearmanjob.sendfail.md) - Відправлення статусу невдалої операції
-   [GearmanJob::setReturn()](gearmanjob.setreturn.md) - Встановлення значення, що повертається
