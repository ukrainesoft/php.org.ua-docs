---
navigation:
  - sessionhandler.destroy.md: '« SessionHandler::destroy'
  - sessionhandler.open.md: 'SessionHandler::open »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::gc'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandler::gc

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandler::gc — Очищає старі сесії

### Опис

```methodsynopsis
public SessionHandler::gc(int $max_lifetime): int|false
```

Очищає сесії з терміном життя, що минув. Викликається випадково зсередини PHP коли сесія стартує або коли викликана функція [session\_start()](function.session-start.md). Частота, з якої вона викликається, ґрунтується на значенні параметрів конфігурації [session.gc\_divisor](session.configuration.md#ini.session.gc-divisor) і [session.gc\_probability](session.configuration.md#ini.session.gc-probability)

Цей метод обертає внутрішній обробник сесії, визначений у налаштуванні ini-файлу [session.save\_handler](session.configuration.md#ini.session.save-handler) який встановлюється перед тим, як визначається даний обробник функції [session\_set\_save\_handler()](function.session-set-save-handler.md)

Якщо цей клас розширюється шляхом успадкування, виклик батьківського методу `gc` виконає код обгортки для цього методу, а також внутрішній обробник. Це дозволить методу бути перевизначеним, або перехопленим та відфільтрованим.

Для додаткової інформації про те, що очікується від реалізації цього методу, дивіться документацію за методом [SessionHandlerInterface::gc()](sessionhandlerinterface.gc.md)

### Список параметрів

`max_lifetime`

Сесії, які не були оновлені протягом останніх `max_lifetime` секунд видаляються.

### Значення, що повертаються

У разі успішного виконання повертає кількість віддалених сесій або **`false`** у разі виникнення помилки. Зауважте, що це значення повертається всередину PHP для обробки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | До цієї версії, у разі успішного виконання ця функція повертала **`true`** |
