---
navigation:
  - sessionhandler.gc.md: '« SessionHandler::gc'
  - sessionhandler.read.md: 'SessionHandler::read »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::open'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandler::open

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandler::open — Ініціалізує сесію

### Опис

```methodsynopsis
public SessionHandler::open(string $path, string $name): bool
```

Створює нову сесію чи повторно ініціалізує існуючу. Викликається зсередини PHP, коли сесія стартує автоматично або за допомогою виклику функції [session\_start()](function.session-start.md)

Цей метод є обгорткою для внутрішнього обробника PHP, визначеного в налаштуванні ini-файлу [session.save\_handler](session.configuration.md#ini.session.save-handler), який встановлюється до визначення обробника викликом функції [session\_set\_save\_handler()](function.session-set-save-handler.md)

Якщо цей клас розширюється шляхом успадкування, виклик батьківського методу `open` виконає код обгортки для цього методу, а також внутрішній обробник. Це дозволить методу бути перевизначеним, або перехопленим та відфільтрованим.

Для додаткової інформації про те, що очікується від реалізації цього методу, дивіться документацію за методом [SessionHandlerInterface::open()](sessionhandlerinterface.open.md)

### Список параметрів

`path`

Шлях яким зберігається/відновлюється сесія.

`name`

Назва сесії.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.

### Дивіться також

-   Опція конфігурації [session.auto-start](session.configuration.md#ini.session.auto-start)
