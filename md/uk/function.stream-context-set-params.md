---
navigation:
  - function.stream-context-set-options.md: « stream\_context\_set\_options
  - function.stream-copy-to-stream.md: stream\_copy\_to\_stream »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_context\_set\_params
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_context\_set\_params

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_context\_set\_params — Встановлює параметри потоку/обгортки/контексту

### Опис

```methodsynopsis
stream_context_set_params(resource $context, array $params): bool
```

Встановлює настройки для зазначеного контексту.

### Список параметрів

`context`

Потік або контекст, до якого будуть використані параметри.

`params`

Асоціативний масив параметрів, які будуть встановлені у наступному форматі: `$params['paramname'] = "paramvalue";`

**Підтримувані параметри**

| Параметр | Назначение |
| --- | --- |
| `notification` | Назва певної користувачем callback-функції, яка буде викликана, коли потоком надсилається повідомлення. Підтримується тільки для обертання потоків [http://](wrappers.http.md) і [ftp://](wrappers.ftp.md) |
| `options` | Массив[опцій та параметрів контексту](context.md) |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [stream\_notification\_callback()](function.stream-notification-callback.md) \- Callback-функція для параметра контексту notification
