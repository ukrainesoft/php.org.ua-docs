---
navigation:
  - gearmanworker.addfunction.md: '« GearmanWorker::addFunction'
  - gearmanworker.addserver.md: 'GearmanWorker::addServer »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::addOptions'
---
# GearmanWorker::addOptions

(PECL gearman >= 0.6.0)

GearmanWorker::addOptions — Додавання налаштувань обробника

### Опис

```methodsynopsis
public GearmanWorker::addOptions(int $option): bool
```

Додає одну або кілька налаштувань до встановлених раніше.

### Список параметрів

`option`

Настройки, що додаються

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanWorker::options()](gearmanworker.options.md) - Отримання налаштувань обробника
-   [GearmanClient::setOptions()](gearmanclient.setoptions.md) - Встановлення налаштувань клієнта
-   [GearmanClient::removeOptions()](gearmanclient.removeoptions.md) - Видалити опції клієнта
