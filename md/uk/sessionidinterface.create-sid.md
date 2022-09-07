---
navigation:
  - class.sessionidinterface.md: « SessionIdInterface
  - class.sessionupdatetimestamphandlerinterface.md: SessionUpdateTimestampHandlerInterface »
  - index.md: PHP Manual
  - class.sessionidinterface.md: SessionIdInterface
title: 'SessionIdInterface::createsid'
---
# SessionIdInterface::createsid

(PHP 5> = 5.5.1, PHP 7, PHP 8)

SessionIdInterface::createsid — Створити ідентифікатор сесії

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

-   [SessionHandler::createsid()](sessionhandler.create-sid.md) - Повертає новий ідентифікатор сесії
