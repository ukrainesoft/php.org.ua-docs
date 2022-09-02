---
navigation:
  - gearmanworker.register.md: '« GearmanWorker::register'
  - gearmanworker.returncode.md: 'GearmanWorker::returnCode »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::removeOptions'
---
# GearmanWorker::removeOptions

(PECL gearman >= 0.6.0)

GearmanWorker::removeOptions — Видалення налаштувань обробника

### Опис

```methodsynopsis
public GearmanWorker::removeOptions(int $option): bool
```

Видаляє одну або кілька опцій обробника.

### Список параметрів

`option`

Налаштування, які потрібно видалити.

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanWorker::options()](gearmanworker.options.md) - Отримання налаштувань обробника
-   [GearmanWorker::setOptions()](gearmanworker.setoptions.md) - Встановлення налаштувань обробника
-   [GearmanWorker::addOptions()](gearmanworker.addoptions.md) - Додавання налаштувань обробника
