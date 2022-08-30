Обумовлені константи

-   [« Прапори, що використовуються у фільтрах](filter.filters.flags.html)
    
-   [Примеры »](filter.examples.html)
    
-   [PHP Manual](index.html)
    
-   [Filter](book.filter.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`INPUT_POST`** (int)

Змінні [POST](reserved.variables.post.html)

**`INPUT_GET`** (int)

Змінні [GET](reserved.variables.get.html)

**`INPUT_COOKIE`** (int)

Змінні [COOKIE](reserved.variables.cookies.html)

**`INPUT_ENV`** (int)

Змінні [ENV](reserved.variables.environment.html)

**`INPUT_SERVER`** (int)

Змінні [SERVER](reserved.variables.server.html)

**`INPUT_SESSION`** (int)

Змінні [SESSION](reserved.variables.session.html). (Ще не реалізовано)

**`INPUT_REQUEST`** (int)

Змінні [REQUEST](reserved.variables.request.html). (Ще не реалізовано)

**`FILTER_FLAG_NONE`** (int)

Не використовувати прапори.

**`FILTER_REQUIRE_SCALAR`** (int)

Прапор використовується для вказівки необхідності скалярного значення як вхідне значення.

**`FILTER_REQUIRE_ARRAY`** (int)

Вимагати масив як вхідне значення.

**`FILTER_FORCE_ARRAY`** (int)

Завжди повертати масив.

**`FILTER_NULL_ON_FAILURE`** (int)

Використовувати NULL замість FALSE у разі виникнення помилки.

**`FILTER_VALIDATE_INT`** (int)

Ідентифікатор фільтра "int".

**`FILTER_VALIDATE_BOOL`** (int)

Псевдонім **`FILTER_VALIDATE_BOOLEAN`**

**`FILTER_VALIDATE_BOOLEAN`** (int)

Ідентифікатор фільтра boolean.

**`FILTER_VALIDATE_FLOAT`** (int)

Ідентифікатор фільтру "float".

**`FILTER_VALIDATE_REGEXP`** (int)

Ідентифікатор фільтра "validateregexp".

**`FILTER_VALIDATE_URL`** (int)

Ідентифікатор фільтра "validateurl".

**`FILTER_VALIDATE_DOMAIN`** (int)

Ідентифікатор фільтра "validateurl". (Доступно з PHP 7.0.0)

**`FILTER_VALIDATE_EMAIL`** (int)

Ідентифікатор фільтра "validateemail".

**`FILTER_VALIDATE_IP`** (int)

Ідентифікатор фільтра "validateip".

**`FILTER_VALIDATE_MAC`** (int)

Ідентифікатор фільтра "validatemacaddress".

**`FILTER_DEFAULT`** (int)

Стандартний ідентифікатор фільтра ("unsaferaw"). Еквівалентно **`FILTER_UNSAFE_RAW`**

**`FILTER_UNSAFE_RAW`** (int)

Ідентифікатор фільтра "unsaferaw".

**`FILTER_SANITIZE_STRING`** (int)

Ідентифікатор фільтра "string". (Оголошено *застарілим*, починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.htmlspecialchars.html)

**`FILTER_SANITIZE_STRIPPED`** (int)

Ідентифікатор фільтра "stripped". (Оголошено *застарілим*, починаючи з PHP 8.1.0, використовуйте замість нього функцію [htmlspecialchars()](function.htmlspecialchars.html)

**`FILTER_SANITIZE_ENCODED`** (int)

Ідентифікатор фільтра "encoded".

**`FILTER_SANITIZE_SPECIAL_CHARS`** (int)

Ідентифікатор фільтра "specialchars".

**`FILTER_SANITIZE_EMAIL`** (int)

Ідентифікатор фільтру "email".

**`FILTER_SANITIZE_URL`** (int)

Ідентифікатор фільтра "URL".

**`FILTER_SANITIZE_NUMBER_INT`** (int)

Ідентифікатор фільтра "numberint".

**`FILTER_SANITIZE_NUMBER_FLOAT`** (int)

Ідентифікатор фільтра "numberfloat".

**`FILTER_SANITIZE_MAGIC_QUOTES`** (int)

Ідентифікатор фільтра "magic"quotes". (*ЗАСТАРІВ* з PHP 7.3.0 та *ВИДАЛЕНО* з PHP 8.0.0, використовуйте замість нього **`FILTER_SANITIZE_ADD_SLASHES`**

**`FILTER_SANITIZE_ADD_SLASHES`** (int)

Ідентифікатор фільтра addslashes". (Доступно з PHP 7.3.0)

**`FILTER_CALLBACK`** (int)

Ідентифікатор фільтра callback.

**`FILTER_FLAG_ALLOW_OCTAL`** (int)

Дозволити вісімковий запис (`0[0-7]+`) у фільтрі "int".

**`FILTER_FLAG_ALLOW_HEX`** (int)

Дозволити шістнадцятковий запис (`0x[0-9a-fA-F]+`) у фільтрі "int".

**`FILTER_FLAG_STRIP_LOW`** (int)

Видаляти символи з ASCII-кодом, меншим за 32.

**`FILTER_FLAG_STRIP_HIGH`** (int)

Видаляти символи з ASCII-кодом, більшим за 127.

**`FILTER_FLAG_STRIP_BACKTICK`** (int)

Видаляє символи зворотного наголосу (гравісу).

**`FILTER_FLAG_ENCODE_LOW`** (int)

Кодувати символи з ASCII-кодом, меншим за 32.

**`FILTER_FLAG_ENCODE_HIGH`** (int)

Кодувати символи з ASCII-кодом, більшим за 127.

**`FILTER_FLAG_ENCODE_AMP`** (int)

Кодувати `&`

**`FILTER_FLAG_NO_ENCODE_QUOTES`** (int)

Не кодувати `'` і `"`

**`FILTER_FLAG_EMPTY_STRING_NULL`** (int)

(На даний момент не використовується.)

**`FILTER_FLAG_ALLOW_FRACTION`** (int)

Дозволити дробову частину у фільтрі "numberfloat".

**`FILTER_FLAG_ALLOW_THOUSAND`** (int)

Дозволити роздільник (`,`) у фільтрі "numberfloat".

**`FILTER_FLAG_ALLOW_SCIENTIFIC`** (int)

Дозволити науковий запис (`e` `E`) у фільтрі "numberfloat".

**`FILTER_FLAG_PATH_REQUIRED`** (int)

Вимагати наявність шляху у фільтрі "validateurl".

**`FILTER_FLAG_QUERY_REQUIRED`** (int)

Вимагати наявність рядка запиту у фільтрі "validateurl".

**`FILTER_FLAG_SCHEME_REQUIRED`** (int)

Вимагати наявність схеми у фільтрі "validateurl". (Оголошено застарілим, починаючи з PHP 7.3.0 і видалений в PHP 8.0.0, так як це і так мається на увазі у фільтрі).

**`FILTER_FLAG_HOST_REQUIRED`** (int)

Вимагати наявність хоста у фільтрі "validateurl". (Оголошено застарілим, починаючи з PHP 7.3.0 і видалений в PHP 8.0.0, так як це і так мається на увазі у фільтрі).

**`FILTER_FLAG_HOSTNAME`** (int)

Вимагати, щоб імена хостів починалися з буквено-цифрових символів та містили лише буквено-цифрові символи чи дефіси. (Доступно з PHP 7.0.0)

**`FILTER_FLAG_IPV4`** (int)

Дозволити лише IPv4-адреси у фільтрі "validateip".

**`FILTER_FLAG_IPV6`** (int)

Дозволити лише IPv6-адреси у фільтрі "validateip".

**`FILTER_FLAG_NO_RES_RANGE`** (int)

Заборонити зарезервовані адреси у фільтрі "validateip".

**`FILTER_FLAG_NO_PRIV_RANGE`** (int)

Заборонити приватні адреси у фільтрі "validateip".

**`FILTER_FLAG_EMAIL_UNICODE`** (int)

Приймати Unicode у локальній частині фільтра "validateemail". (Доступно з PHP 7.1.0)