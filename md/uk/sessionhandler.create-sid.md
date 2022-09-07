---
navigation:
  - sessionhandler.close.md: '« SessionHandler::close'
  - sessionhandler.destroy.md: 'SessionHandler::destroy »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::createsid'
---
# SessionHandler::createsid

(PHP 5> = 5.5.1, PHP 7, PHP 8)

SessionHandler::createsid — Повертає новий ідентифікатор сесії

### Опис

```methodsynopsis
public SessionHandler::create_sid(): string
```

Генерує та повертає новий ідентифікатор сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ідентифікатор сесії допустимий для оброблювача сесії за промовчанням.

### Дивіться також

-   [sessionid()](function.session-id.md) - Отримує та/або встановлює ідентифікатор поточної сесії
-   [sessioncreateid()](function.session-create-id.md) - створює новий ідентифікатор сесії
