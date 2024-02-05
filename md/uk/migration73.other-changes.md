---
navigation:
  - migration73.deprecated.md: '« Функціонал, оголошений застарілим у PHP 7.3.x'
  - migration73.windows-support.md: Підтримка Windows »
  - index.md: PHP Manual
  - migration73.md: Міграція з PHP 7.2.x на PHP 7.3.x
title: Інші зміни
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Інші зміни

### Ядро PHP

#### Функція set(raw)cookie приймає аргумент $option

Функції [setcookie()](function.setcookie.md) і [setrawcookie()](function.setrawcookie.md) тепер також підтримують таке оголошення (сигнатуру):

```methodsynopsis
setcookie(string $name, string $value = "", array $options = []): bool
```

где`$options` - асоціативний масив, який може мати будь-який із ключів `"expires"` `"path"` `"domain"` `"secure"` `"httponly"`и`"samesite"`

#### Нові ini-директиви syslog

Наступні ini-директиви додані для налаштування логування, якщо для опції [error\_log](errorfunc.configuration.md#ini.error-log)установлено значение`syslog` :

[syslog.facility](errorfunc.configuration.md#ini.syslog.facility)

Вказує тип програми, яка реєструє повідомлення.

[syslog.filter](errorfunc.configuration.md#ini.syslog.filter)

Задає тип фільтра для фільтрації повідомлень з типами фільтрів, що підтримуються - `all` `no-ctrl`и`ascii`. Починаючи з PHP 7.3.8, також доступний тип `raw`, що відновлює поведінку системного журналу у попередніх версіях PHP. Цей фільтр також вплине на дзвінки [syslog()](function.syslog.md)

[syslog.ident](errorfunc.configuration.md#ini.syslog.ident)

Задає рядок ident, який додається перед кожним повідомленням.

#### Складальник сміття

Улучшен[збір циклічних посилань](features.gc.collecting-cycles.md)що може призвести до значних покращень продуктивності.

#### Різне

Функция[var\_export()](function.var-export.md) тепер експортує об'єкти [stdClass](class.stdclass.md) як масив, приведений до об'єкта (`(object) array( ... )`), вместо использования несуществующего метода**stdClass::\_\_setState()**

Функция[debug\_zval\_dump()](function.debug-zval-dump.md) змінена для відображення рекурсивних масивів та об'єктів так само, як і [var\_dump()](function.var-dump.md). Тепер вона не відображає їх двічі.

Функції [array\_push()](function.array-push.md) і [array\_unshift()](function.array-unshift.md) тепер також можуть бути викликані одним аргументом, що особливо зручно в поєднанні з оператором поширення.

### Інтерактивний відладчик PHP

Видалені константи, що не використовуються. **`PHPDBG_FILE`** **`PHPDBG_METHOD`** **`PHPDBG_LINENO`**и**`PHPDBG_FUNC`**

### Менеджер процесів FastCGI

Тепер також доступна функція [getallheaders()](function.getallheaders.md)

### Бібліотека Client URL (cURL)

Тепер потрібна бібліотека libcurl версії ≥ 7.15.5.

### Фільтрування даних

**`FILTER_VALIDATE_FLOAT`** тепер також підтримує параметр `thousand`, який визначає набір дозволених символів-розділювачів тисяч. Значення за замовчуванням (`"',."`) повністю зворотно сумісне з попередніми версіями PHP.

**`FILTER_SANITIZE_ADD_SLASHES`** був доданий як псевдонім фільтра `magic_quotes` **`FILTER_SANITIZE_MAGIC_QUOTES`**). Фильтр`magic_quotes` підлягає видаленню у майбутніх версіях PHP.

### FTP

Стандартний режим змінено на `binary`

### Функції інтернаціоналізації

Константа\*\*`Normalizer::NONE`\*\* оголошена застарілою, коли PHP скомпільовано з ICU версії ≥ 56.

Введена константа\*\*`Normalizer::FORM_KC_CF`\*\*в качестве аргумента[Normalizer::normalize()](normalizer.normalize.md)для нормализации`NFKC_Casefold`; доступна, коли є ICU ≥56.

### Об'єктна нотація JavaScript (JSON)

Доданий новий прапор **`JSON_THROW_ON_ERROR`**, який можна використовувати з [json\_decode()](function.json-decode.md) або [json\_encode()](function.json-encode.md) і змушує ці функції викидати новий виняток [JsonException](class.jsonexception.md) у разі виникнення помилки замість того, щоб встановлювати глобальний стан помилки, який вилучається за допомогою [json\_last\_error()](function.json-last-error.md) і [json\_last\_error\_msg()](function.json-last-error-msg.md). . **`JSON_PARTIAL_OUTPUT_ON_ERROR`**имеет приоритет над**`JSON_THROW_ON_ERROR`**

### Мультибайтові рядки

Конфігураційна опція **\--with-libmbfl** більше недоступне.

### ODBC (Unified)

Поддержка`ODBCRouter`и`Birdstep`, включая ini-директиву`birdstep.max_links` було видалено.

### OPcache

Видалено ini-директиву `opcache.inherited_hack`. Це значення вже ігнорувалося з PHP 5.3.0.

### OpenSSL

Додані опції потоку ssl `min_proto_version`и`max_proto_version`, а також відповідні константи для можливих значень протоколу TLS.

### Регулярні вирази (сумісні з Perl)

[Модуль PCRE](book.pcre.md) було оновлено до PCRE2, що може призвести до незначних змін у поведінці (наприклад, діапазони символів у класах тепер інтерпретуються суворіше) і доповнює існуючий синтаксис регулярних виразів.

Функция[preg\_quote()](function.preg-quote.md) тепер також екранує символ `'#'`

### Microsoft SQL Server та функції Sybase (PDO\_DBLIB)

Добавлен атрибут\*\*`PDO::DBLIB_ATTR_SKIP_EMPTY_ROWSETS`\*\* для автоматичного пропуску порожніх наборів рядків.

Добавлен атрибут\*\*`PDO::DBLIB_ATTR_TDS_VERSION`\*\* що представляє версію TDS.

Стовпці DATETIME2 тепер обробляються як стовпці DATETIME.

### Функції SQLite (PDO\_SQLITE)

Бази даних SQLite3 тепер можна відкрити в режимі лише для читання, встановивши новий атрибут **`PDO::SQLITE_ATTR_OPEN_FLAGS`**на значение**`PDO::SQLITE_OPEN_READONLY`**

### Обробка сесій

Функция[session\_set\_cookie\_params()](function.session-set-cookie-params.md) тепер також підтримує таке оголошення (сигнатуру):

```methodsynopsis
session_set_cookie_params(array $options): bool
```

где`$options` - асоціативний масив, який може мати будь-який із ключів `"lifetime"` `"path"` `"domain"` `"secure"` `"httponly"`и`"samesite"`Соответственно, возвращаемое значение[session\_get\_cookie\_params()](function.session-get-cookie-params.md) тепер також має елемент із ключем `"samesite"`. Крім того, нова ini-опція `session.cookie_samesite` для встановлення за промовчанням директиви SameSite для cookies. За замовчуванням використовується значення `""` (порожній рядок), тому директива SameSite не вказана. Може бути встановлена ​​на значення `"Lax"`или`"Strict"`, яке встановлює відповідне значення директиви SameSite.

### Tidy

Сборка вместе[» tidyp](https://github.com/petdance/tidyp) Тепер також підтримується прозоро. Оскільки tidyp не пропонує API для отримання дати релізу, [tidy\_get\_release()](tidy.getrelease.md) і [tidy::getRelease()](tidy.getrelease.md) повертає значення `'unknown'` в цьому випадку.

### XML-парсер

Значення callback-функції, що повертається [xml\_set\_external\_entity\_ref\_handler()](function.xml-set-external-entity-ref-handler.md) більше не ігнорується, якщо модуль був зібраний із бібліотекою libxml. Раніше значення, що поверталося, ігнорувалося, а парсинг ніколи не припинявся.

### Zip

Складання з використанням libzip, що входить до PHP, не рекомендується, але все ж таки можлива шляхом додавання **\--without-libzip** у конфігурацію.

### Стиснення Zlib

Добавлен параметр контекста zlib/level для[обгортки compress.zlib](wrappers.compression.md), щоб полегшити встановлення бажаного рівня стиснення.
