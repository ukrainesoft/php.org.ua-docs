---
navigation:
  - function.stream-context-set-option.html: « streamcontextsetoption
  - function.stream-copy-to-stream.html: streamcopyтоstream »
  - index.html: PHP Manual
  - ref.stream.html: Функції для роботи з потоками
title: streamcontextsetparams
---
# streamcontextsetparams

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamcontextsetparams — Встановлює параметри потоку/обгортки/контексту

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
| `notification` | Назва певної користувачем callback-функції, яка буде викликана, коли потоком надсилається повідомлення. Підтримується тільки для обертання потоків [http://](wrappers.http.html) і [ftp://](wrappers.ftp.html) |
| `options` | Масив [опций и параметров контекста](context.html) |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [streamnotificationcallback()](function.stream-notification-callback.html) - Callback-функція для параметра контексту notification
