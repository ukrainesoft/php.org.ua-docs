---
navigation:
  - sessionhandler.create-sid.html: '« SessionHandler::createsid'
  - sessionhandler.gc.md: 'SessionHandler::gc »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::destroy'
---
# SessionHandler::destroy

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandler::destroy — Знищує сесію

### Опис

```methodsynopsis
public SessionHandler::destroy(string $id): bool
```

Знищує сесію. Викликається зсередини PHP за допомогою функції [sessionregenerateid()](function.session-regenerate-id.html) (маю на увазі, що параметр `$destroy` встановлений в **`true`**, функції [sessiondestroy()](function.session-destroy.html) або коли виклик [sessiondecode()](function.session-decode.html) невдалий.

Цей метод є обгорткою для внутрішнього обробника PHP, визначеного в налаштуванні ini-файлу [session.savehandler](session.configuration.html#ini.session.save-handler), який встановлюється до оброблювача викликом [sessionsetsavehandler()](function.session-set-save-handler.html)

Якщо цей клас розширюється шляхом наслідування, то виклик батьківського методу `destroy` виконає код обгортки, а отже код внутрішнього оброблювача. Це дозволяє бути перевизначеним, перехопленим або відфільтрованим.

Для додаткової інформації дивіться посібник з функції [SessionHandlerInterface::destroy()](sessionhandlerinterface.destroy.md)

### Список параметрів

`id`

Ідентифікатор сесії, що знищується.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.
