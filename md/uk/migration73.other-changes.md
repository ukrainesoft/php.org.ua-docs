---
navigation:
  - migration73.deprecated.html: '« Функціонал, оголошений застарілим у PHP 7.3.x'
  - migration73.windows-support.html: Поддержка Windows »
  - index.html: PHP Manual
  - migration73.html: Миграция с PHP 7.2.x на PHP 7.3.x
title: Інші зміни
---
## Інші зміни

### Ядро PHP

#### Функція set(raw)cookie приймає аргумент $option

Функції [setcookie()](function.setcookie.html) і [setrawcookie()](function.setrawcookie.html) тепер також підтримують таке оголошення (сигнатуру):

```methodsynopsis
setcookie(string $name, string $value = "", array $options = []): bool
```

де `$options` - асоціативний масив, який може мати будь-який із ключів `"expires"` `"path"` `"domain"` `"secure"` `"httponly"` і `"samesite"`

#### Нові ini-директиви syslog

Наступні ini-директиви додані для налаштування логування, якщо для опції [errorlog](errorfunc.configuration.html#ini.error-log) встановлено значення `syslog`

[syslog.facility](errorfunc.configuration.html#ini.syslog.facility)

Вказує тип програми, яка реєструє повідомлення.

[syslog.filter](errorfunc.configuration.html#ini.syslog.filter)

Задає тип фільтра для фільтрації повідомлень з типами фільтрів, що підтримуються - `all` `no-ctrl` і `ascii`. Починаючи з PHP 7.3.8, також доступний тип `raw`, що відновлює поведінку системного журналу у попередніх версіях PHP. Цей фільтр також вплине на дзвінки [syslog()](function.syslog.html)

[syslog.ident](errorfunc.configuration.html#ini.syslog.ident)

Задає рядок ident, який додається перед кожним повідомленням.

#### Складальник сміття

Поліпшено [збір циклічних посилань](features.gc.collecting-cycles.html)що може призвести до значних покращень продуктивності.

#### Різне

Функція [varexport()](function.var-export.html) тепер експортує об'єкти **stdClass** як масив, приведений до об'єкта (`(object) array( ... )`), замість використання неіснуючого методу **stdClass::setState()**

Функція [debugzvaldump()](function.debug-zval-dump.html) змінена для відображення рекурсивних масивів та об'єктів так само, як і [vardump()](function.var-dump.html). Тепер вона не відображає їх двічі.

Функції [arraypush()](function.array-push.html) і [arrayunshift()](function.array-unshift.html) тепер також можуть бути викликані одним аргументом, що особливо зручно в поєднанні з оператором поширення.

### Інтерактивний відладчик PHP

Видалені константи, що не використовуються. **`PHPDBG_FILE`** **`PHPDBG_METHOD`** **`PHPDBG_LINENO`** і **`PHPDBG_FUNC`**

### Менеджер процесів FastCGI

Тепер також доступна функція [getallheaders()](function.getallheaders.html)

### Бібліотека Client URL (cURL)

Тепер потрібна бібліотека libcurl версії ≥ 7.15.5.

### Фільтрування даних

**`FILTER_VALIDATE_FLOAT`** тепер також підтримує параметр `thousand`, який визначає набір дозволених символів-розділювачів тисяч. Значення за замовчуванням (`"',."`) повністю зворотно сумісне з попередніми версіями PHP.

**`FILTER_SANITIZE_ADD_SLASHES`** був доданий як псевдонім фільтра `magic_quotes` **`FILTER_SANITIZE_MAGIC_QUOTES`**). Фільтр `magic_quotes` підлягає видаленню у майбутніх версіях PHP.

### FTP

Стандартний режим змінено на `binary`

### Функції інтернаціоналізації

Константа **`Normalizer::NONE`** оголошена застарілою, коли PHP скомпільовано з ICU версії ≥ 56.

Введено константу **`Normalizer::FORM_KC_CF`** як аргумент [Normalizer::normalize()](normalizer.normalize.html) для нормалізації `NFKC_Casefold`; доступна, коли є ICU ≥56.

### Об'єктна нотація JavaScript (JSON)

Доданий новий прапор **`JSON_THROW_ON_ERROR`**, який можна використовувати з [jsondecode()](function.json-decode.html) або [jsonencode()](function.json-encode.html) і змушує ці функції викидати новий виняток [JsonException](class.jsonexception.html) у разі виникнення помилки, замість того, щоб встановлювати глобальний стан помилки, який вилучається за допомогою [jsonlasterror()](function.json-last-error.html) і [jsonlasterrormsg()](function.json-last-error-msg.html). . **`JSON_PARTIAL_OUTPUT_ON_ERROR`** має пріоритет над **`JSON_THROW_ON_ERROR`**

### Мультибайтові рядки

Конфігураційна опція **\-with-libmbfl** більше недоступне.

### ODBC (Unified)

Підтримка `ODBCRouter` і `Birdstep`, включаючи ini-директиву `birdstep.max_links` було видалено.

### OPcache

Видалено ini-директиву `opcache.inherited_hack`. Це значення вже ігнорувалося з PHP 5.3.0.

### OpenSSL

Додані опції потоку ssl `min_proto_version` і `max_proto_version`, а також відповідні константи для можливих значень протоколу TLS.

### Регулярні вирази (сумісні з Perl)

[Модуль PCRE](book.pcre.html) було оновлено до PCRE2, що може призвести до незначних змін у поведінці (наприклад, діапазони символів у класах тепер інтерпретуються суворіше) і доповнює існуючий синтаксис регулярних виразів.

Функція [pregquote()](function.preg-quote.html) тепер також екранує символ `'#'`

### Microsoft SQL Server та функції Sybase (PDODBLIB)

Доданий атрибут **`PDO::DBLIB_ATTR_SKIP_EMPTY_ROWSETS`** для автоматичного пропуску порожніх наборів рядків.

Доданий атрибут **`PDO::DBLIB_ATTR_TDS_VERSION`** що представляє версію TDS.

Стовпці DATETIME2 тепер обробляються як стовпці DATETIME.

### Функції SQLite (PDOSQLITE)

Бази даних SQLite3 тепер можна відкрити в режимі лише для читання, встановивши новий атрибут **`PDO::SQLITE_ATTR_OPEN_FLAGS`** на значення **`PDO::SQLITE_OPEN_READONLY`**

### Обробка сесій

Функція [sessionsetcookieparams()](function.session-set-cookie-params.html) тепер також підтримує таке оголошення (сигнатуру):

```methodsynopsis
session_set_cookie_params(array $options): bool
```

де `$options` - асоціативний масив, який може мати будь-який із ключів `"lifetime"` `"path"` `"domain"` `"secure"` `"httponly"` і `"samesite"`. Відповідно, значення, що повертається [sessiongetcookieparams()](function.session-get-cookie-params.html) тепер також має елемент із ключем `"samesite"`. Крім того, нова ini-опція `session.cookie_samesite` для встановлення за промовчанням директиви SameSite для cookies. За замовчуванням використовується значення `""` (порожній рядок), тому директива SameSite не вказана. Може бути встановлена ​​на значення `"Lax"` або `"Strict"`, яке встановлює відповідне значення директиви SameSite.

### Tidy

Складання разом [» tidyp](https://github.com/petdance/tidyp) Тепер також підтримується прозоро. Оскільки tidyp не пропонує API для отримання дати релізу, [tidygetrelease()](tidy.getrelease.html) і [tidy::getRelease()](tidy.getrelease.html) повертає значення `'unknown'` в цьому випадку.

### XML-парсер

Значення callback-функції, що повертається [xmlsetexternalentityrefhandler()](function.xml-set-external-entity-ref-handler.html) більше не ігнорується, якщо модуль був зібраний із бібліотекою libxml. Раніше значення, що поверталося, ігнорувалося, а парсинг ніколи не припинявся.

### Zip

Складання з використанням libzip, що входить до PHP, не рекомендується, але все ж таки можлива шляхом додавання **\-without-libzip** у конфігурацію.

### Стиснення Zlib

Додано параметр контексту zlib/level для [обёртки compress.zlib](wrappers.compression.html), щоб полегшити встановлення бажаного рівня стиснення.
