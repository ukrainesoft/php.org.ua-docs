---
navigation:
  - class.sessionhandler.md: « SessionHandler
  - sessionhandler.create-sid.html: 'SessionHandler::createsid »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::close'
---
# SessionHandler::close

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandler::close — Закриває сесію

### Опис

```methodsynopsis
public SessionHandler::close(): bool
```

Закриває поточну сесію. Цей метод автоматично викликається із PHP під час закриття сесії або безпосередньо викликом функції [sessionwriteclose()](function.session-write-close.md) (яка спочатку викликає функцію [SessionHandler::write()](sessionhandler.write.md)

Цей метод є обертанням внутрішнього обробника сесій PHP, визначеного в налаштуванні ini-файлу [session.savehandler](session.configuration.html#ini.session.save-handler), яка встановлюється перед тим, як обробник активується функцією [sessionsetsavehandler()](function.session-set-save-handler.md)

Якщо цей клас розширюється шляхом наслідування, то виклик батьківського методу `close` виконає код обгортки, а отже код внутрішнього оброблювача. Це дозволяє методу бути перевизначеним чи перехопленим.

Додаткову інформацію про те, які дії очікуються від цього методу дивіться посібник з методу [SessionHandlerInterface::close()](sessionhandlerinterface.close.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.
