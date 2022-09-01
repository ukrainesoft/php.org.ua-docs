---
navigation:
  - function.session-save-path.html: « sessionsavepath
  - function.session-set-save-handler.html: sessionsetsavehandler »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionsetcookieparams
---
# sessionsetcookieparams

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionsetcookieparams — Встановлює параметри сесійної cookie

### Опис

```methodsynopsis
session_set_cookie_params(    int $lifetime_or_options,    ?string $path = null,    ?string $domain = null,    ?bool $secure = null,    ?bool $httponly = null): bool
```

Альтернативна сигнатура доступна з PHP 7.3.0:

```methodsynopsis
session_set_cookie_params(array $lifetime_or_options): bool
```

```methodsynopsis
session_set_cookie_params(array $options): bool
```

Встановлює параметри cookie, визначені у php.ini. Ефект цієї функції зберігається лише під час виконання скрипта. Таким чином, потрібно викликати **sessionsetcookieparams()** для кожного запиту та перед кожним викликом [sessionstart()](function.session-start.html)

Ця функція оновлює поточні ini-значення відповідних ключів конфігурації PHP ini, які можна отримати за допомогою [iniget()](function.ini-get.html)

### Список параметрів

`lifetime_or_options`

Якщо використовувати першу сигнатуру, [время жизни](session.configuration.html#ini.session.cookie-lifetime) сесійної куки, задане в секундах.

Якщо використовувати другу сигнатуру, то асоціативний масив (array), який може мати будь-який ключ `lifetime` `path` `domain` `secure` `httponly` і `samesite`. Значення мають той самий зміст, як описано у параметрах з відповідним ім'ям. Значення елемента `samesite` повинно бути або `Lax`, або `Strict`. Якщо жодна з допустимих опцій не вказана, її значення за умовчанням збігаються зі значеннями за промовчанням для явних параметрів. Якщо елемент `samesite` не вказано, атрибут cookie SameSite не встановлений.

`path`

[Шлях](session.configuration.html#ini.session.cookie-path) в домені, де буде працювати cookie. Використовуйте одну косу ('/') для всіх шляхів у домені.

`domain`

[Домен](session.configuration.html#ini.session.cookie-domain) cookie, наприклад '[www.php.net'](http://www.php.net'). Щоб зробити cookies видимими для всіх піддоменів, перед ім'ям домену потрібно встановити точку, наприклад '.php.net'.

`secure`

Якщо **`true`**, то cookies будуть передаватися тільки через [захищені](session.configuration.html#ini.session.cookie-secure) з'єднання.

`httponly`

Якщо встановлено **`true`**, то PHP спробує відправити прапор [httponly](session.configuration.html#ini.session.cookie-httponly) при налаштуванні сесійної cookie.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `path` `domain` `secure` і `httponly` тепер можуть бути **`null`** |
|  | Додано альтернативний підпис, що підтримує масив опцій `lifetime_or_options`. Цей підпис також підтримує налаштування cookie-атрибута SameSite. |
|  | Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Раніше повертала тип void. |

### Дивіться також

-   [session.cookielifetime](session.configuration.html#ini.session.cookie-lifetime)
-   [session.cookiepath](session.configuration.html#ini.session.cookie-path)
-   [session.cookiedomain](session.configuration.html#ini.session.cookie-domain)
-   [session.cookiesecure](session.configuration.html#ini.session.cookie-secure)
-   [session.cookiehttponly](session.configuration.html#ini.session.cookie-httponly)
-   [session.cookiesamesite](session.configuration.html#ini.session.cookie-samesite)
-   [sessiongetcookieparams()](function.session-get-cookie-params.html) - Повертає параметри cookie сесії
