---
navigation:
  - sessionhandlerinterface.destroy.md: '« SessionHandlerInterface::destroy'
  - sessionhandlerinterface.open.md: 'SessionHandlerInterface::open »'
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::gc'
---
# SessionHandlerInterface::gc

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::gc — Очищає старі сесії

### Опис

```methodsynopsis
public SessionHandlerInterface::gc(int $max_lifetime): int|false
```

Очищає сесії з терміном життя, що минув. Викликається функцією [sessionstart()](function.session-start.html), і ґрунтується на опціях [session.gcdivisor](session.configuration.html#ini.session.gc-divisor) [session.gcprobability](session.configuration.html#ini.session.gc-probability) і [session.gcmaxlifetime](session.configuration.html#ini.session.gc-maxlifetime)

### Список параметрів

`max_lifetime`

Сесії, які не оновлювалися протягом `max_lifetime` секунд, будуть видалені.

### Значення, що повертаються

Повертає кількість віддалених сесій у разі успішного виконання або **`false`** у разі виникнення помилки. Зауважте, що це значення повертається всередині PHP для обробки.

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії функція повертала **`true`** у разі успішного виконання. |
