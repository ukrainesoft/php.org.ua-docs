---
navigation:
  - migration71.deprecated.md: '« Функціонал, оголошений застарілим у PHP 7.1.x'
  - migration71.other-changes.md: Інші зміни »
  - index.md: PHP Manual
  - migration71.md: Міграція з PHP 7.0.x на PHP 7.1.x
title: Змінені функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Змінені функції

### Ядро PHP

-   [getopt()](function.getopt.md)має третій, необов'язковий параметр, в який записується індекс, на якому зупинилася обробка. Змінна у цей параметр передається за посиланням.
-   В[getenv()](function.getenv.md)більше не обов'язково передавати параметр. Якщо параметр не заданий, повертаються всі поточні змінні оточення у вигляді асоціативного масиву.
-   [get\_headers()](function.get-headers.md)тепер має додатковий параметр для дозволу передачі певного потокового контексту користувачем.
-   [output\_reset\_rewrite\_vars()](function.output-reset-rewrite-vars.md)більше не скидає сесійні змінні перезаписи URL-адреси.
-   [parse\_url()](function.parse-url.md)тепер більш вимоглива та підтримує RFC3986.
-   [unpack()](function.unpack.md)тепер має третій необов'язковий параметр визначення зміщення з якого починати розпаковування.

### Файлова система

-   [file\_get\_contents()](function.file-get-contents.md)тепер приймає негативні значення усунення початку пошуку, якщо потік підтримує усунення.
-   [tempnam()](function.tempnam.md)тепер видає повідомлення при поверненні до системного тимчасового каталогу.

### JSON

-   [json\_encode()](function.json-encode.md)тепер приймає нову опцію,**`JSON_UNESCAPED_LINE_TERMINATORS`**, для заборони екранування символів U+2028 та U+2029, коли передається\*\*`JSON_UNESCAPED_UNICODE`\*\*

### Багатобайтові рядки

-   [mb\_ereg()](function.mb-ereg.md)Тепер відхиляє некоректні послідовності байтів.
-   [mb\_ereg\_replace()](function.mb-ereg-replace.md)Тепер відхиляє некоректні послідовності байтів.

### PDO

-   [PDO::lastInsertId()](pdo.lastinsertid.md)для PostgreSQL тепер породжує помилку, якщо в поточній сесії (з'єднанні) не викликано`nextval`

### PostgreSQL

-   [pg\_last\_notice()](function.pg-last-notice.md)тепер приймає необов'язковий параметр, що задає операцію. Використовується одна з наступних констант:**`PGSQL_NOTICE_LAST`** **`PGSQL_NOTICE_ALL`**или**`PGSQL_NOTICE_CLEAR`**
-   [pg\_fetch\_all()](function.pg-fetch-all.md)тепер приймає другий, необов'язковий параметр для завдання типу результату (аналогічно третьому параметру[pg\_fetch\_array()](function.pg-fetch-array.md)
-   [pg\_select()](function.pg-select.md)тепер приймає четвертий, необов'язковий параметр для завдання типу результату (аналогічно третьому параметру[pg\_fetch\_array()](function.pg-fetch-array.md)

### Сесії

-   [session\_start()](function.session-start.md) тепер повертає \*\*`false`\*\*і більше не ініціалізує[$\_SESSION](reserved.variables.session.md)коли вона не змогла запустити сесію.
