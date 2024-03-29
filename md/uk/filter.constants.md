---
navigation:
  - filter.filters.flags.md: « Прапори для фільтрів
  - filter.examples.md: Приклади »
  - index.md: PHP Manual
  - book.filter.md: Filter
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`INPUT_POST`**(int)

Змінні [POST](reserved.variables.post.md)

**`INPUT_GET`**(int)

Змінні [GET](reserved.variables.get.md)

**`INPUT_COOKIE`**(int)

Змінні [COOKIE](reserved.variables.cookies.md)

**`INPUT_ENV`**(int)

Змінні [ENV](reserved.variables.environment.md)

**`INPUT_SERVER`**(int)

Змінні [SERVER](reserved.variables.server.md)

**`INPUT_SESSION`**(int)

Змінні [SESSION](reserved.variables.session.md). (Ще не реалізовано)

**`INPUT_REQUEST`**(int)

Змінні [REQUEST](reserved.variables.request.md). (Ще не реалізовано)

**`FILTER_FLAG_NONE`**(int)

Не використовувати прапори.

**`FILTER_REQUIRE_SCALAR`**(int)

Прапор використовується для вказівки необхідності скалярного значення як вхідне значення.

**`FILTER_REQUIRE_ARRAY`**(int)

Вимагати масив як вхідне значення.

**`FILTER_FORCE_ARRAY`**(int)

Завжди повертати масив.

**`FILTER_NULL_ON_FAILURE`**(int)

Використовувати NULL замість FALSE у разі виникнення помилки.

**`FILTER_VALIDATE_INT`**(int)

Ідентифікатор фільтра "int".

**`FILTER_VALIDATE_BOOL`**(int)

Псевдоним\*\*`FILTER_VALIDATE_BOOLEAN`\*\*

**`FILTER_VALIDATE_BOOLEAN`**(int)

Ідентифікатор фільтра boolean.

**`FILTER_VALIDATE_FLOAT`**(int)

Ідентифікатор фільтру "float".

**`FILTER_VALIDATE_REGEXP`**(int)

Ідентифікатор фільтра "validate\_regexp".

**`FILTER_VALIDATE_URL`**(int)

Ідентифікатор фільтра "validate\_url".

**`FILTER_VALIDATE_DOMAIN`**(int)

Ідентифікатор фільтра "validate\_url". (Доступно з PHP 7.0.0)

**`FILTER_VALIDATE_EMAIL`**(int)

Ідентифікатор фільтра "validate\_email".

**`FILTER_VALIDATE_IP`**(int)

Ідентифікатор фільтра "validate\_ip".

**`FILTER_VALIDATE_MAC`**(int)

Ідентифікатор фільтра "validate\_mac\_address".

**`FILTER_DEFAULT`**(int)

Стандартний ідентифікатор фільтра ("unsafe\_raw"). Еквівалентно **`FILTER_UNSAFE_RAW`**

**`FILTER_UNSAFE_RAW`**(int)

Ідентифікатор фільтра "unsafe\_raw".

**`FILTER_SANITIZE_STRING`**(int)

Ідентифікатор фільтра "string". (Оголошено *застарілим*, починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.mdspecialchars.md)

**`FILTER_SANITIZE_STRIPPED`**(int)

Ідентифікатор фільтра "stripped". (Оголошено *застарілим*, починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.mdspecialchars.md)

**`FILTER_SANITIZE_ENCODED`**(int)

Ідентифікатор фільтра "encoded".

**`FILTER_SANITIZE_SPECIAL_CHARS`**(int)

Ідентифікатор фільтра "special\_chars".

**`FILTER_SANITIZE_EMAIL`**(int)

Ідентифікатор фільтру "email".

**`FILTER_SANITIZE_URL`**(int)

Ідентифікатор фільтра "URL".

**`FILTER_SANITIZE_NUMBER_INT`**(int)

Ідентифікатор фільтра "number\_int".

**`FILTER_SANITIZE_NUMBER_FLOAT`**(int)

Ідентифікатор фільтра "number\_float".

**`FILTER_SANITIZE_MAGIC_QUOTES`**(int)

Ідентифікатор фільтра "magic"\_quotes". (*ЗАСТАРІВ* з PHP 7.3.0 та *ВИДАЛЕНО* з PHP 8.0.0, використовуйте замість нього **`FILTER_SANITIZE_ADD_SLASHES`**

**`FILTER_SANITIZE_ADD_SLASHES`**(int)

Ідентифікатор фільтра add\_slashes". (Доступно з PHP 7.3.0)

**`FILTER_CALLBACK`**(int)

Ідентифікатор фільтра callback.

**`FILTER_FLAG_ALLOW_OCTAL`**(int)

Дозволити вісімковий запис (`0[0-7]+`) у фільтрі "int".

**`FILTER_FLAG_ALLOW_HEX`**(int)

Дозволити шістнадцятковий запис (`0x[0-9a-fA-F]+`) у фільтрі "int".

**`FILTER_FLAG_STRIP_LOW`**(int)

Видаляти символи з ASCII-кодом, меншим за 32.

**`FILTER_FLAG_STRIP_HIGH`**(int)

Видаляти символи з ASCII-кодом, більшим за 127.

**`FILTER_FLAG_STRIP_BACKTICK`**(int)

Видаляє символи зворотного наголосу (гравісу).

**`FILTER_FLAG_ENCODE_LOW`**(int)

Кодувати символи з ASCII-кодом, меншим за 32.

**`FILTER_FLAG_ENCODE_HIGH`**(int)

Кодувати символи з ASCII-кодом, більшим за 127.

**`FILTER_FLAG_ENCODE_AMP`**(int)

Кодувати `&`

**`FILTER_FLAG_NO_ENCODE_QUOTES`**(int)

Не кодувати `'`и`"`

**`FILTER_FLAG_EMPTY_STRING_NULL`**(int)

(На даний момент не використовується.)

**`FILTER_FLAG_ALLOW_FRACTION`**(int)

Дозволити дробову частину у фільтрі "number\_float".

**`FILTER_FLAG_ALLOW_THOUSAND`**(int)

Дозволити роздільник (`,`) у фільтрі "number\_float".

**`FILTER_FLAG_ALLOW_SCIENTIFIC`**(int)

Дозволити науковий запис (`e` `E`) у фільтрі "number\_float".

**`FILTER_FLAG_PATH_REQUIRED`**(int)

Вимагати наявність шляху у фільтрі "validate\_url".

**`FILTER_FLAG_QUERY_REQUIRED`**(int)

Вимагати наявність рядка запиту у фільтрі "validate\_url".

**`FILTER_FLAG_SCHEME_REQUIRED`**(int)

Вимагати наявність схеми у фільтрі "validate\_url". (Оголошено застарілим, починаючи з PHP 7.3.0 і видалений в PHP 8.0.0, так як це і так мається на увазі у фільтрі).

**`FILTER_FLAG_HOST_REQUIRED`**(int)

Вимагати наявність хоста у фільтрі "validate\_url". (Оголошено застарілим, починаючи з PHP 7.3.0 і видалений в PHP 8.0.0, так як це і так мається на увазі у фільтрі).

**`FILTER_FLAG_HOSTNAME`**(int)

Вимагати, щоб імена хостів починалися з буквено-цифрових символів та містили лише буквено-цифрові символи чи дефіси. (Доступно з PHP 7.0.0)

**`FILTER_FLAG_IPV4`**(int)

Дозволити лише IPv4-адреси у фільтрі "validate\_ip".

**`FILTER_FLAG_IPV6`**(int)

Дозволити лише IPv6-адреси у фільтрі "validate\_ip".

**`FILTER_FLAG_NO_RES_RANGE`**(int)

Заборонити зарезервовані адреси у фільтрі "validate\_ip".

**`FILTER_FLAG_NO_PRIV_RANGE`**(int)

Заборонити приватні адреси у фільтрі "validate\_ip".

**`FILTER_FLAG_EMAIL_UNICODE`**(int)

Приймати Unicode у локальній частині фільтра "validate\_email". (Доступно з PHP 7.1.0)
