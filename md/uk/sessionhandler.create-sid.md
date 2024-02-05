---
navigation:
  - sessionhandler.close.md: '« SessionHandler::close'
  - sessionhandler.destroy.md: 'SessionHandler::destroy »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::create\_sid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandler::create\_sid

(PHP 5 >= 5.5.1, PHP 7, PHP 8)

SessionHandler::create\_sid — Повертає новий ідентифікатор сесії

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

-   [session\_id()](function.session-id.md) \- Отримує та/або встановлює ідентифікатор поточної сесії
-   [session\_create\_id()](function.session-create-id.md) \- створює новий ідентифікатор сесії
