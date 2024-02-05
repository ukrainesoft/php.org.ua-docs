---
navigation:
  - class.sessionidinterface.md: « SessionIdInterface
  - class.sessionupdatetimestamphandlerinterface.md: SessionUpdateTimestampHandlerInterface »
  - index.md: PHP Manual
  - class.sessionidinterface.md: SessionIdInterface
title: 'SessionIdInterface::create\_sid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionIdInterface::create\_sid

(PHP 5 >= 5.5.1, PHP 7, PHP 8)

SessionIdInterface::create\_sid — Створити ідентифікатор сесії

### Опис

```methodsynopsis
public SessionIdInterface::create_sid(): string
```

Створює новий ідентифікатор сесії. Функція автоматично виконується, коли потрібно створити новий ідентифікатор сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Новий ідентифікатор сесії Зауважте, що це значення повертається всередині PHP для обробки.

### Дивіться також

-   [SessionHandler::create\_sid()](sessionhandler.create-sid.md) \- Повертає новий ідентифікатор сесії
