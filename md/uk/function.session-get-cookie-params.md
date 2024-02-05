---
navigation:
  - function.session-gc.md: « session\_gc
  - function.session-id.md: session\_id »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_get\_cookie\_params
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_get\_cookie\_params

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_get\_cookie\_params — Повертає параметри cookie сесії

### Опис

```methodsynopsis
session_get_cookie_params(): array
```

Повертає параметри cookie сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з інформацією про cookie поточної сесії, що містить такі елементи:

-   ["lifetime"](session.configuration.md#ini.session.cookie-lifetime) \- час життя cookie за секунди.
-   ["path"](session.configuration.md#ini.session.cookie-path) \- шлях, де розміщена інформація, що зберігається.
-   ["domain"](session.configuration.md#ini.session.cookie-domain) \- Домен cookie.
-   ["secure"](session.configuration.md#ini.session.cookie-secure) \- cookie повинні передаватись лише через безпечні з'єднання.
-   ["httponly"](session.configuration.md#ini.session.cookie-httponly) \- cookie можуть бути доступні лише за протоколом HTTP.
-   ["samesite"](session.configuration.md#ini.session.cookie-samesite) \- керує міждоменною відправкою cookie.

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Доданий елемент "samesite" у масив, що повертається. |

### Дивіться також

-   [session.cookie\_lifetime](session.configuration.md#ini.session.cookie-lifetime)
-   [session.cookie\_path](session.configuration.md#ini.session.cookie-path)
-   [session.cookie\_domain](session.configuration.md#ini.session.cookie-domain)
-   [session.cookie\_secure](session.configuration.md#ini.session.cookie-secure)
-   [session.cookie\_httponly](session.configuration.md#ini.session.cookie-httponly)
-   [session.cookie\_samesite](session.configuration.md#ini.session.cookie-samesite)
-   [session\_set\_cookie\_params()](function.session-set-cookie-params.md) \- Встановлює параметри сесійної cookie
