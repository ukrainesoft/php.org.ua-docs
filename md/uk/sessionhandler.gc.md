Очищує старі сесії

-   [« SessionHandler::destroy](sessionhandler.destroy.md)
    
-   [SessionHandler::open »](sessionhandler.open.md)
    
-   [PHP Manual](index.md)
    
-   [SessionHandler](class.sessionhandler.md)
    
-   Очищує старі сесії
    

# SessionHandler::gc

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandler::gc — Очищає старі сесії

### Опис

```methodsynopsis
public SessionHandler::gc(int $max_lifetime): int|false
```

Очищає сесії з терміном життя, що минув. Викликається випадково зсередини PHP коли сесія стартує або коли викликана функція [sessionstart()](function.session-start.html). Частота, з якої вона викликається, ґрунтується на значенні параметрів конфігурації [session.gcdivisor](session.configuration.html#ini.session.gc-divisor) і [session.gcprobability](session.configuration.html#ini.session.gc-probability)

Цей метод обертає внутрішній обробник сесії, визначений у налаштуванні ini-файлу [session.savehandler](session.configuration.html#ini.session.save-handler) який встановлюється перед тим, як визначається даний обробник функції [sessionsetsavehandler()](function.session-set-save-handler.html)

Якщо цей клас розширюється шляхом успадкування, виклик батьківського методу `gc` виконає код обгортки для цього методу, а також внутрішній обробник. Це дозволить методу бути перевизначеним, або перехопленим та відфільтрованим.

Для додаткової інформації про те, що очікується від реалізації цього методу, дивіться документацію за методом [SessionHandlerInterface::gc()](sessionhandlerinterface.gc.md)

### Список параметрів

`max_lifetime`

Сесії, які не були оновлені протягом останніх `max_lifetime` секунд видаляються.

### Значення, що повертаються

У разі успішного виконання повертає кількість віддалених сесій або **`false`** у разі виникнення помилки. Зауважте, що це значення повертається всередину PHP для обробки.

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії, у разі успішного виконання ця функція повертала **`true`** |