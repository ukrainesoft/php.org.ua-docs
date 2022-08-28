Змінені функції

-   [« Функционал, объявленный устаревшим в PHP 7.1.x](migration71.deprecated.html)
    
-   [Прочие изменения »](migration71.other-changes.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.0.x на PHP 7.1.x](migration71.html)
    
-   Змінені функції
    

## Змінені функції

### Ядро PHP

-   [getopt()](function.getopt.html) має третій, необов'язковий параметр, в який записується індекс, на якому зупинилася обробка. Змінна у цей параметр передається за посиланням.
-   У [getenv()](function.getenv.html) більше не обов'язково передавати параметр. Якщо параметр не заданий, повертаються всі поточні змінні оточення у вигляді асоціативного масиву.
-   [get\_headers()](function.get-headers.html) тепер має додатковий параметр для дозволу передачі певного потокового контексту користувачем.
-   [output\_reset\_rewrite\_vars()](function.output-reset-rewrite-vars.html) більше не скидає сесійні змінні перезаписи URL-адреси.
-   [parse\_url()](function.parse-url.html) тепер більш вимоглива та підтримує RFC3986.
-   [unpack()](function.unpack.html) тепер має третій необов'язковий параметр визначення зміщення з якого починати розпаковування.

### Файлова система

-   [file\_get\_contents()](function.file-get-contents.html) тепер приймає негативні значення усунення початку пошуку, якщо потік підтримує усунення.
-   [tempnam()](function.tempnam.html) тепер видає повідомлення при поверненні до системного тимчасового каталогу.

### JSON

-   [json\_encode()](function.json-encode.html) тепер приймає нову опцію, **`JSON_UNESCAPED_LINE_TERMINATORS`**, для заборони екранування символів U+2028 та U+2029, коли передається **`JSON_UNESCAPED_UNICODE`**

### Багатобайтові рядки

-   [mb\_ereg()](function.mb-ereg.html) тепер відхиляє некоректні послідовності байтів.
-   [mb\_ereg\_replace()](function.mb-ereg-replace.html) тепер відхиляє некоректні послідовності байтів.

### PDO

-   [PDO::lastInsertId()](pdo.lastinsertid.html) для PostgreSQL тепер породжує помилку, якщо в поточній сесії (з'єднанні) не викликано `nextval`

### PostgreSQL

-   [pg\_last\_notice()](function.pg-last-notice.html) тепер приймає необов'язковий параметр, який задає операцію. Використовується одна з наступних констант: **`PGSQL_NOTICE_LAST`** **`PGSQL_NOTICE_ALL`** або **`PGSQL_NOTICE_CLEAR`**
-   [pg\_fetch\_all()](function.pg-fetch-all.html) тепер приймає другий, необов'язковий параметр для завдання типу результату (аналогічно третьому параметру [pg\_fetch\_array()](function.pg-fetch-array.html)
-   [pg\_select()](function.pg-select.html) тепер приймає четвертий, необов'язковий параметр для завдання типу результату (аналогічно третьому параметру [pg\_fetch\_array()](function.pg-fetch-array.html)

### Сесії

-   [session\_start()](function.session-start.html) тепер повертає **`false`** і більше не ініціалізує [$\_SESSION](reserved.variables.session.html)коли вона не змогла запустити сесію.