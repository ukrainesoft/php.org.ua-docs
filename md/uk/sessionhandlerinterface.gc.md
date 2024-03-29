---
navigation:
  - sessionhandlerinterface.destroy.md: '« SessionHandlerInterface::destroy'
  - sessionhandlerinterface.open.md: 'SessionHandlerInterface::open »'
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::gc'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandlerInterface::gc

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::gc — Очищає старі сесії

### Опис

```methodsynopsis
public SessionHandlerInterface::gc(int $max_lifetime): int|false
```

Очищає сесії з терміном життя, що минув. Викликається функцією [session\_start()](function.session-start.md), і ґрунтується на опціях [session.gc\_divisor](session.configuration.md#ini.session.gc-divisor) [session.gc\_probability](session.configuration.md#ini.session.gc-probability) і [session.gc\_maxlifetime](session.configuration.md#ini.session.gc-maxlifetime)

### Список параметрів

`max_lifetime`

Сесії, які не оновлювалися протягом `max_lifetime` секунд, будуть видалені.

### Значення, що повертаються

Повертає кількість віддалених сесій у разі успішного виконання або **`false`** у разі виникнення помилки. Зауважте, що це значення повертається всередині PHP для обробки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | До цієї версії функція повертала **`true`** у разі успішного виконання. |
