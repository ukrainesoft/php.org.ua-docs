---
navigation:
  - event.construct.md: '« Event::\_\_construct'
  - event.delsignal.md: 'Event::delSignal »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::del'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Event::del

(PECL event >= 1.2.6-beta)

Event::del — Перевести подію в пасивний стан

### Опис

```methodsynopsis
public
   Event::del(): bool
```

Видаляє подію з набору подій, що відстежуються, тобто. переводить їх у стан не-ожидания.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [Event::add()](event.add.md) \- Перевести подію у стан очікування
