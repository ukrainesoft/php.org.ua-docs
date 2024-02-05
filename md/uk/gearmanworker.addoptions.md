---
navigation:
  - gearmanworker.addfunction.md: '« GearmanWorker::addFunction'
  - gearmanworker.addserver.md: 'GearmanWorker::addServer »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::addOptions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanWorker::addOptions

(PECL gearman >= 0.6.0)

GearmanWorker::addOptions — Додавання налаштувань обробника

### Опис

```methodsynopsis
public GearmanWorker::addOptions(int $option): true
```

Додає одну або кілька налаштувань до встановлених раніше.

### Список параметрів

`option`

Настройки, що додаються

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [GearmanWorker::options()](gearmanworker.options.md) \- Отримання налаштувань обробника
-   [GearmanClient::setOptions()](gearmanclient.setoptions.md) \- Встановлення налаштувань клієнта
-   [GearmanClient::removeOptions()](gearmanclient.removeoptions.md) \- Видалити опції клієнта
