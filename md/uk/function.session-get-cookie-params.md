Повертає параметри cookie сесії

-   [« session\_gc](function.session-gc.html)
    
-   [session\_id »](function.session-id.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Повертає параметри cookie сесії
    

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

-   [session.cookie\_lifetime](session.configuration.html#ini.session.cookie-lifetime)
-   [session.cookie\_path](session.configuration.html#ini.session.cookie-path)
-   [session.cookie\_domain](session.configuration.html#ini.session.cookie-domain)
-   [session.cookie\_secure](session.configuration.html#ini.session.cookie-secure)
-   [session.cookie\_httponly](session.configuration.html#ini.session.cookie-httponly)
-   [session.cookie\_samesite](session.configuration.html#ini.session.cookie-samesite)
-   [session\_set\_cookie\_params()](function.session-set-cookie-params.html) - Встановлює параметри сесійної cookie