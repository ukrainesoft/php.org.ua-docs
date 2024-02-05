---
navigation:
  - gearmanworker.echo.md: '« GearmanWorker::echo'
  - gearmanworker.geterrno.md: 'GearmanWorker::getErrno »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::error'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanWorker::error

(PECL gearman >= 0.5.0)

GearmanWorker::error — Отримання останньої виявленої помилки

### Опис

```methodsynopsis
public GearmanWorker::error(): string|false
```

Повертає рядок із повідомленням про останню виявлену помилку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Строка с описанием ошибки или\*\*`false`\*\*, якщо повідомлення про помилку відсутнє.

### Дивіться також

-   [GearmanWorker::getErrno()](gearmanworker.geterrno.md) \- Отримання номера помилки
