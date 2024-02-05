---
navigation:
  - function.session-save-path.md: « session\_save\_path
  - function.session-set-save-handler.md: session\_set\_save\_handler »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_set\_cookie\_params
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_set\_cookie\_params

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_set\_cookie\_params — Встановлює параметри сесійної cookie

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

Встановлює параметри cookie, визначені у php.ini. Ефект цієї функції зберігається лише під час виконання скрипта. Таким чином, потрібно викликати **session\_set\_cookie\_params()** для кожного запиту та перед кожним викликом [session\_start()](function.session-start.md)

Ця функція оновлює поточні ini-значення відповідних ключів конфігурації PHP ini, які можна отримати за допомогою [ini\_get()](function.ini-get.md)

### Список параметрів

`lifetime_or_options`

Якщо використовувати першу сигнатуру, [час життя](session.configuration.md#ini.session.cookie-lifetime) сесійної куки, задане в секундах.

Якщо використовувати другу сигнатуру, то асоціативний масив (array), який може мати будь-який ключ `lifetime` `path` `domain` `secure` `httponly`и`samesite`. Значення мають той самий зміст, як описано у параметрах з відповідним ім'ям. Значення елемента `samesite` повинно бути або `Lax`, либо`Strict`. Якщо жодна з допустимих опцій не вказана, її значення за умовчанням збігаються зі значеннями за промовчанням для явних параметрів. Якщо елемент `samesite`не указан, cookie-атрибут SameSite не установлен.

`path`

[Шлях](session.configuration.md#ini.session.cookie-path) в домені, де буде працювати cookie. Використовуйте одну косу ('/') для всіх шляхів у домені.

`domain`

[Домен](session.configuration.md#ini.session.cookie-domain) cookie, наприклад '[www.php.net'](http://www.php.net'). . Щоб зробити cookies видимими для всіх піддоменів, перед ім'ям домену потрібно встановити точку, наприклад '.php.net'.

`secure`

Якщо **`true`**, то cookies будут передаваться только через[захищені](session.configuration.md#ini.session.cookie-secure)соединения.

`httponly`

Если установлено\*\*`true`\*\*, то PHP спробує відправити прапор [httponly](session.configuration.md#ini.session.cookie-httponly)при настройке сессионной cookie.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `path` `domain` `secure`и`httponly` тепер можуть бути **`null`** |
| 7.3.0 | Додано альтернативний підпис, що підтримує масив опцій `lifetime_or_options`. . Цей підпис також підтримує налаштування cookie-атрибута SameSite. |
| 7.2.0 | Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Раніше повертала тип void. |

### Дивіться також

-   [session.cookie\_lifetime](session.configuration.md#ini.session.cookie-lifetime)
-   [session.cookie\_path](session.configuration.md#ini.session.cookie-path)
-   [session.cookie\_domain](session.configuration.md#ini.session.cookie-domain)
-   [session.cookie\_secure](session.configuration.md#ini.session.cookie-secure)
-   [session.cookie\_httponly](session.configuration.md#ini.session.cookie-httponly)
-   [session.cookie\_samesite](session.configuration.md#ini.session.cookie-samesite)
-   [session\_get\_cookie\_params()](function.session-get-cookie-params.md) \- Повертає параметри cookie сесії
