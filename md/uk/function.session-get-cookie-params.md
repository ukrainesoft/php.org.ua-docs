---
navigation:
  - function.session-gc.html: « sessionгк
  - function.session-id.html: sessionid »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessiongetcookieparams
---
# sessiongetcookieparams

(PHP 4, PHP 5, PHP 7, PHP 8)

sessiongetcookieparams — Повертає параметри cookie сесії

### Опис

```methodsynopsis
session_get_cookie_params(): array
```

Повертає параметри cookie сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з інформацією про cookie поточної сесії, що містить такі елементи:

-   ["lifetime"](session.configuration.html#ini.session.cookie-lifetime) - час життя cookie за секунди.
-   ["path"](session.configuration.html#ini.session.cookie-path) - шлях, де розміщена інформація, що зберігається.
-   ["domain"](session.configuration.html#ini.session.cookie-domain) - Домен cookie.
-   ["secure"](session.configuration.html#ini.session.cookie-secure) - cookie повинні передаватись лише через безпечні з'єднання.
-   ["httponly"](session.configuration.html#ini.session.cookie-httponly) - cookie можуть бути доступні лише за протоколом HTTP.
-   ["samesite"](session.configuration.html#ini.session.cookie-samesite) - керує міждоменною відправкою cookie.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий елемент "samesite" у масив, що повертається. |

### Дивіться також

-   [session.cookielifetime](session.configuration.html#ini.session.cookie-lifetime)
-   [session.cookiepath](session.configuration.html#ini.session.cookie-path)
-   [session.cookiedomain](session.configuration.html#ini.session.cookie-domain)
-   [session.cookiesecure](session.configuration.html#ini.session.cookie-secure)
-   [session.cookiehttponly](session.configuration.html#ini.session.cookie-httponly)
-   [session.cookiesamesite](session.configuration.html#ini.session.cookie-samesite)
-   [sessionsetcookieparams()](function.session-set-cookie-params.md) - Встановлює параметри сесійної cookie
