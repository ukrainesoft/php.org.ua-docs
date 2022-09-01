---
navigation:
  - migration71.deprecated.md: '« Функціонал, оголошений застарілим у PHP 7.1.x'
  - migration71.other-changes.html: Прочие изменения »
  - index.md: PHP Manual
  - migration71.md: Миграция с PHP 7.0.x на PHP 7.1.x
title: Змінені функції
---
## Змінені функції

### Ядро PHP

-   [getopt()](function.getopt.md) має третій, необов'язковий параметр, в який записується індекс, на якому зупинилася обробка. Змінна у цей параметр передається за посиланням.
-   У [getenv()](function.getenv.md) більше не обов'язково передавати параметр. Якщо параметр не заданий, повертаються всі поточні змінні оточення у вигляді асоціативного масиву.
-   [getheaders()](function.get-headers.md) тепер має додатковий параметр для дозволу передачі певного потокового контексту користувачем.
-   [outputresetrewritevars()](function.output-reset-rewrite-vars.md) більше не скидає сесійні змінні перезаписи URL-адреси.
-   [parseurl()](function.parse-url.md) тепер більш вимоглива та підтримує RFC3986.
-   [unpack()](function.unpack.md) тепер має третій необов'язковий параметр визначення зміщення з якого починати розпаковування.

### Файлова система

-   [filegetcontents()](function.file-get-contents.md) тепер приймає негативні значення усунення початку пошуку, якщо потік підтримує усунення.
-   [tempnam()](function.tempnam.md) тепер видає повідомлення при поверненні до системного тимчасового каталогу.

### JSON

-   [jsonencode()](function.json-encode.md) тепер приймає нову опцію, **`JSON_UNESCAPED_LINE_TERMINATORS`**, для заборони екранування символів U+2028 та U+2029, коли передається **`JSON_UNESCAPED_UNICODE`**

### Багатобайтові рядки

-   [мбereg()](function.mb-ereg.md) тепер відхиляє некоректні послідовності байтів.
-   [мбeregreplace()](function.mb-ereg-replace.md) тепер відхиляє некоректні послідовності байтів.

### PDO

-   [PDO::lastInsertId()](pdo.lastinsertid.md) для PostgreSQL тепер породжує помилку, якщо в поточній сесії (з'єднанні) не викликано `nextval`

### PostgreSQL

-   [пгlastnotice()](function.pg-last-notice.md) тепер приймає необов'язковий параметр, який задає операцію. Використовується одна з наступних констант: **`PGSQL_NOTICE_LAST`** **`PGSQL_NOTICE_ALL`** або **`PGSQL_NOTICE_CLEAR`**
-   [пгfetchall()](function.pg-fetch-all.html) тепер приймає другий, необов'язковий параметр для завдання типу результату (аналогічно третьому параметру [пгfetcharray()](function.pg-fetch-array.md)
-   [пгselect()](function.pg-select.html) тепер приймає четвертий, необов'язковий параметр для завдання типу результату (аналогічно третьому параметру [пгfetcharray()](function.pg-fetch-array.md)

### Сесії

-   [sessionstart()](function.session-start.md) тепер повертає **`false`** і більше не ініціалізує [SESSION](reserved.variables.session.md)коли вона не змогла запустити сесію.
