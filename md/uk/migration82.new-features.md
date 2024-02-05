---
navigation:
  - migration82.md: « Міграція з PHP 8.1.x на PHP 8.2.x
  - migration82.new-functions.md: Нові функції »
  - index.md: PHP Manual
  - migration82.md: Міграція з PHP 8.1.x на PHP 8.2.x
title: Нова функціональність
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Нова функціональність

### Ядро PHP

#### Атрибут SensitiveParameter

Добавлен атрибут`#[\SensitiveParameter]` для редагування конфіденційних даних у трасуваннях стека викликів.

#### INI-директива error\_log\_mode

Додано INI-директиву [error\_log\_mode](errorfunc.configuration.md#ini.error-log-mode), яка дозволяє встановити дозволи для файлу журналу помилок.

#### Властивості перерахувань у константних виразах

Тепер можна отримувати властивості [перерахувань](language.enumerations.md) у константних виразах.

#### Поліпшення системи типів

Тепер можна використовувати null та false як самостійні типи.

Доданий тип true.

Тепер можна комбінувати перетин та об'єднання типів. Тип має бути записаний у вигляді DNF.

#### Константи у трейтах

Тепер у трейтах можна визначати константи.

#### Класи, доступні лише для читання

Добавлена поддержка[readonly для класів](language.oop5.basic.md#language.oop5.basic.class.readonly)

### cURL

Добавлена опция\*\*`CURLINFO_EFFECTIVE_METHOD`\*\*, яка повертає останній використаний метод HTTP у значенні функції, що повертається [curl\_getinfo()](function.curl-getinfo.md)

Стало доступно[безліч нових констант](migration82.constants.md#migration82.constants.curl)из libcurl 7.62 - 7.80.

Добавлена функция[curl\_upkeep()](function.curl_upkeep.md) для виконання будь-яких перевірок відновлення з'єднання.

### DBA

Драйвер LMDB тепер приймає прапори **`DBA_LMDB_USE_SUB_DIR`** або **`DBA_LMDB_NO_SUB_DIR`**, щоб визначити, чи має він створювати підкаталог чи ні під час створення файлу бази даних.

### OCI8

Додано INI-директиву [oci8.prefetch\_lob\_size](oci8.configuration.md#ini.oci8.prefetch-lob-size)и функция[oci\_set\_prefetch\_lob()](function.oci-set-prefetch-lob.md) для налаштування продуктивності LOB-запитів шляхом зменшення кількості обходів між PHP та базами даних Oracle під час вибірки LOBS. Її можна використовувати з Oracle Database 12.2 або пізнішою версією.

### OpenSSL

Додано підтримку AEAD-алгоритму chacha20-poly1305.

### ODBC

Додані функції [odbc\_connection\_string\_is\_quoted()](function.odbc-connection-string-is-quoted.md) [odbc\_connection\_string\_should\_quote()](function.odbc-connection-string-should-quote.md) і [odbc\_connection\_string\_quote()](function.odbc-connection-string-quote.md). В основному вони використовуються всередині самих модулів ODBC та PDO\_ODBC, але полегшення модульного тестування тепер доступні ззовні. Крім цього, ними можна скористатися для екранування рядка з програм користувача.

### PCRE

Добавлена поддержка модификатора`n`(NO\_AUTO\_CAPTURE), який робить прості групи `(xyz)` не перехоплюються. Перехоплюються лише іменовані групи типу `(?<name>xyz)`. Це впливає тільки на те, які групи перехоплюються, як і раніше, можна використовувати нумеровані посилання на підшаблони і масив збігів, як і раніше, буде містити нумеровані результати.

### Random

Це новий модуль, який організовує та консолідує існуючі реалізації, пов'язані з генераторами випадкових чисел. У нових та покращених ДСЛ усунуто проблеми, пов'язані з областю їх застосування.
