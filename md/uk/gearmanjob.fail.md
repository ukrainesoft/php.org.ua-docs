---
navigation:
  - gearmanjob.exception.md: '« GearmanJob::exception'
  - gearmanjob.functionname.md: 'GearmanJob::functionName »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::fail'
---
# GearmanJob::fail

(PECL gearman <= 0.5.0)

GearmanJob::fail — Надсилання статусу невдалої операції (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::fail(): bool
```

Посилає статус про невдалу обробку, вказуючи, що завдання завершилося невдало з відомих причин (на відміну невдалого завершення, коли викидається виняток).

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendFail()](gearmanjob.sendfail.md) у версії 0.6.0 модуля Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendException()](gearmanjob.sendexception.md) - Відправлення виключення завдання, що виконується
-   [GearmanJob::setReturn()](gearmanjob.setreturn.md) - Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.md) - Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.md) - Відправлення попередження
