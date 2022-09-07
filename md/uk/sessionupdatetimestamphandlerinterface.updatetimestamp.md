---
navigation:
  - class.sessionupdatetimestamphandlerinterface.md: « SessionUpdateTimestampHandlerInterface
  - sessionupdatetimestamphandlerinterface.validateid.md: 'SessionUpdateTimestampHandlerInterface::validateId »'
  - index.md: PHP Manual
  - class.sessionupdatetimestamphandlerinterface.md: SessionUpdateTimestampHandlerInterface
title: 'SessionUpdateTimestampHandlerInterface::updateTimestamp'
---
# SessionUpdateTimestampHandlerInterface::updateTimestamp

(PHP 7, PHP 8)

SessionUpdateTimestampHandlerInterface::updateTimestamp — Оновити позначку часу

### Опис

```methodsynopsis
public SessionUpdateTimestampHandlerInterface::updateTimestamp(string $id, string $data): bool
```

Оновлює позначку часу останньої зміни сеансу. Функція автоматично виконується під час оновлення сеансу.

### Список параметрів

`id`

Ідентифікатор сесії

`data`

Дані сесії.

### Значення, що повертаються

Повертає **`true`**, якщо мітку часу оновлено, **`false`** в іншому випадку. Зауважте, що це значення повертається всередині PHP для обробки.
