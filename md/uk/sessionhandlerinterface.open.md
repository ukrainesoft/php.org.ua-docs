---
navigation:
  - sessionhandlerinterface.gc.md: '« SessionHandlerInterface::gc'
  - sessionhandlerinterface.read.md: 'SessionHandlerInterface::read »'
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::open'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandlerInterface::open

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::open — Ініціалізує сесію

### Опис

```methodsynopsis
public SessionHandlerInterface::open(string $path, string $name): bool
```

Повторно ініціалізує існуючу сесію чи створює нову. Викликається коли сесія стартує або коли викликана функція [session\_start()](function.session-start.md)

### Список параметрів

`path`

Шлях, яким зберігається/відновлюється сесія.

`name`

Назва сесії.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.

### Дивіться також

-   [session\_name()](function.session-name.md) \- Отримати чи встановити ім'я поточної сесії
-   Опція конфігурації [session.auto-start](session.configuration.md#ini.session.auto-start)
