---
navigation:
  - sessionhandler.close.html: '« SessionHandler::close'
  - sessionhandler.destroy.html: 'SessionHandler::destroy »'
  - index.html: PHP Manual
  - class.sessionhandler.html: SessionHandler
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

-   [sessionid()](function.session-id.html) - Отримує та/або встановлює ідентифікатор поточної сесії
-   [sessioncreateid()](function.session-create-id.html) - створює новий ідентифікатор сесії
