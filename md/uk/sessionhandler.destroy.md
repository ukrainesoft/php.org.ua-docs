---
navigation:
  - sessionhandler.create-sid.md: '« SessionHandler::create\_sid'
  - sessionhandler.gc.md: 'SessionHandler::gc »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::destroy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandler::destroy

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandler::destroy — Знищує сесію

### Опис

```methodsynopsis
public SessionHandler::destroy(string $id): bool
```

Знищує сесію. Викликається зсередини PHP за допомогою функції [session\_regenerate\_id()](function.session-regenerate-id.md)(подразумевается, что параметр`$destroy`установлен в\*\*`true`\*\*, функції [session\_destroy()](function.session-destroy.md) або коли виклик [session\_decode()](function.session-decode.md)неудачен.

Цей метод є обгорткою для внутрішнього обробника PHP, визначеного в налаштуванні ini-файлу [session.save\_handler](session.configuration.md#ini.session.save-handler), який встановлюється до оброблювача викликом [session\_set\_save\_handler()](function.session-set-save-handler.md)

Якщо цей клас розширюється шляхом наслідування, то виклик батьківського методу `destroy` виконає код обгортки, а отже код внутрішнього оброблювача. Це дозволяє бути перевизначеним, перехопленим або відфільтрованим.

Для дополнительной информации смотрите руководство по функции[SessionHandlerInterface::destroy()](sessionhandlerinterface.destroy.md)

### Список параметрів

`id`

Ідентифікатор сесії, що знищується.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.
