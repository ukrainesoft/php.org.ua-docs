---
navigation:
  - migration82.deprecated.md: « Застаріла функціональність
  - migration82.windows-support.md: Підтримка Windows »
  - index.md: PHP Manual
  - migration82.md: Міграція з PHP 8.1.x на PHP 8.2.x
title: Інші зміни
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Інші зміни

### Зміни у ядрі

Тип[iterable](language.types.iterable.md) тепер є вбудованим під час компіляції псевдонімом для array |[Traversable](class.traversable.md). Тому повідомлення про помилки, пов'язані з типом `iterable`, будуть тепер використовувати сигнатуру `array|Traversable`. Тип Reflection зберігається для одиночного `iterable`(и`?iterable`) для создания[ReflectionNamedType](class.reflectionnamedtype.md)с именем`iterable`, проте використання `iterable` в об'єднаннях типів буде перетворено на `array|Traversable`

Формат дати надісланих файлів cookie тепер `'D, d M Y H:i:s \G\M\T'`; раніше він був `'D, d-M-Y H:i:s T'`

### Зміни у модулях SAPI

#### CLI

Потоки STDOUT, STDERR та STDIN більше не закриваються при знищенні ресурсів, що найчастіше відбувається після завершення роботи CLI. Однак, як і раніше, можна явно закрити ці потоки за допомогою функції [fclose()](function.fclose.md) та подібних функцій.

### Змінені функції

#### Ядро PHP

Функції [strcmp()](function.strcmp.md) [strcasecmp()](function.strcasecmp.md) [strncmp()](function.strncmp.md) [strncasecmp()](function.strncasecmp.md) і [substr\_compare()](function.substr-compare.md), що використовують бінарне безпечне порівняння рядків, тепер повертають `-1` и

#### DBA

У функции[dba\_open()](function.dba-open.md) і [dba\_popen()](function.dba-popen.md)теперь следующая принудительная сигнатура:

```methodsynopsis
dba_open(    string $path,    string $mode,    ?string $handler = null,    int $permission = 0644,    int $map_size = 0,    ?int $flags = null): resource|false
```

Необов'язковий аргумент skip функції [dba\_fetch()](function.dba-fetch.md) тепер знаходиться в кінці відповідно до семантики користувальницького простору PHP. Тепер його сигнатура виглядає так:

```methodsynopsis
dba_fetch(string|array $key, resource $handle, int $skip): string|false
```

Попередня сигнатура:

```methodsynopsis
dba_fetch(string|array $key, int $skip, resource $handle): string|false
```

як і раніше, приймається, але рекомендується використовувати новий стандартний варіант.

#### Random

Функції [random\_bytes()](function.random-bytes.md) і [random\_int()](function.random-int.md) тепер викидають виняток **\\Random\\RandomException** у разі помилок CSPRNG. Раніше натомість викидався звичайний виняток **\\Exception**

#### SPL

Параметр`iterator`функций[iterator\_to\_array()](function.iterator-to-array.md) і [iterator\_count()](function.iterator-count.md)расширен до[iterable](language.types.iterable.md)из[Iterator](class.iterator.md)дозволяючи передавати масиви.

### Інші зміни у модулях

#### Date

Свойства[DatePeriod](class.dateperiod.md) тепер оголошено правильно.

#### Intl

Примірники [IntlBreakIterator](class.intlbreakiterator.md) [IntlRuleBasedBreakIterator](class.intlrulebasedbreakiterator.md) [IntlCodePointBreakIterator](class.intlcodepointbreakiterator.md) [IntlPartsIterator](class.intlpartsiterator.md) [IntlCalendar](class.intlcalendar.md) [Collator](class.collator.md) [IntlIterator](class.intliterator.md) [UConverter](class.uconverter.md) [IntlDateFormatter](class.intldateformatter.md) [IntlDatePatternGenerator](class.intldatepatterngenerator.md) [MessageFormatter](class.messageformatter.md) [ResourceBundle](class.resourcebundle.md) [Spoofchecker](class.spoofchecker.md) [IntlTimeZone](class.intltimezone.md) і [Transliterator](class.transliterator.md) більше не є серіалізованими. Раніше їх можна було серіалізувати, але за десеріалізації виходили непридатні об'єкти або виникали помилки.

#### MySQLi

Підтримка libmysql була видалена, і тепер неможливо скомпілювати mysqli з libmysql. З цього моменту модуль mysqli можна компілювати лише за допомогою mysqlnd. Усі функції libmysql, недоступні в mysqlnd, були видалені:

-   Властивість reconnect для[mysqli\_driver](class.mysqli-driver.md)
-   INI-директива[mysqli.reconnect](mysqli.configuration.md#ini.mysqli.reconnect)
-   Константа\*\*`MYSQLI_IS_MARIADB`\*\*застаріла

#### OCI8

Мінімальна необхідна версія бібліотеки Oracle Client тепер 11.2.

#### PCRE

Тепер підтримуються символи NUL (`\0`) у рядках шаблонів.

#### Сесія

Спроба змінити INI-директиву [session.cookie\_samesite](session.configuration.md#ini.session.cookie-samesite), коли сесія активна або висновок вже надісланий, тепер буде невдалою та видасть попередження. Ця зміна уніфікує поведінку за аналогією з усіма іншими налаштуваннями INI-директив сесії.

#### SQLite3

[sqlite3.defensive](sqlite3.configuration.md#ini.sqlite3.defensive) тепер **`INI_USER`**

#### Стандартні функції

Функция[getimagesize()](function.getimagesize.md) тепер повідомляє фактичні розміри, біти та канали зображень AVIF. Раніше розміри повідомлялися як 0x0, а біти та канали взагалі не повідомлялися.

#### Tidy

Свойства класса[tidy](class.tidy.md) тепер оголошено правильно. А властивості класу [tidyNode](class.tidynode.md) тепер правильно оголошено як доступні лише для читання.

#### Zip

Модуль Zip було оновлено до версії 1.20.0, до якої додано такі методи:

-   [ZipArchive::clearError()](ziparchive.clearerror.md)
-   [ZipArchive::getStreamName()](ziparchive.getstreamname.md)
-   [ZipArchive::getStreamIndex()](ziparchive.getstreamindex.md)

### Зміни у роботі з INI-файлами

До цілих INI-параметрів додано підтримку двійкових (`0b` `0B`) та вісімкових (`0o` `0O`) префіксів. Цілочисельні INI-параметри, що починаються з нуля ( ), продовжують інтерпретуватися як вісімкове ціле число.

При розборі деяких неправильно відформатованих значень тепер видаватиметься попередження, якщо це мовчки ігнорувалося раніше. Для зворотної сумісності інтерпретація цих значень змінилася. Це впливає на наступні опції:

-   [bcmath.scale](bc.configuration.md#ini.bcmath.scale)
-   [com.code\_page](com.configuration.md#ini.com.code-page)
-   [default\_socket\_timeout](filesystem.configuration.md#ini.default-socket-timeout)
-   fiber.stack\_size
-   [hard\_timeout](ini.core.md#ini.hard-timeout)
-   [intl.error\_level](intl.configuration.md#ini.intl.error-level)
-   [ldap.max\_links](ldap.configuration.md#ini.ldap.max_links)
-   [max\_input\_nesting\_level](info.configuration.md#ini.max-input-nesting-level)
-   [max\_input\_vars](info.configuration.md#ini.max-input-vars)
-   [mbstring.regex\_retry\_limit](mbstring.configuration.md#ini.mbstring.regex-retry-limit)
-   [mbstring.regex\_stack\_limit](mbstring.configuration.md#ini.mbstring.regex-stack-limit)
-   [mysqli.allow\_local\_infile](mysqli.configuration.md#ini.mysqli.allow-local-infile)
-   [mysqli.allow\_persistent](mysqli.configuration.md#ini.mysqli.allow-persistent)
-   [mysqli.default\_port](mysqli.configuration.md#ini.mysqli.default-port)
-   [mysqli.max\_links](mysqli.configuration.md#ini.mysqli.max-links)
-   [mysqli.max\_persistent](mysqli.configuration.md#ini.mysqli.max-persistent)
-   [mysqli.rollback\_on\_cached\_plink](mysqli.configuration.md#ini.mysqli.rollback-on-cached-plink)
-   [mysqlnd.log\_mask](mysqlnd.config.md#ini.mysqlnd.log-mask)
-   [mysqlnd.mempool\_default\_size](mysqlnd.config.md#ini.mysqlnd.mempool-default-size)
-   [mysqlnd.net\_read\_buffer\_size](mysqlnd.config.md#ini.mysqlnd.net-read-buffer-size)
-   [mysqlnd.net\_read\_timeout](mysqlnd.config.md#ini.mysqlnd.net-read-timeout)
-   [oci8.default\_prefetch](oci8.configuration.md#ini.oci8.default-prefetch)
-   [oci8.max\_persistent](oci8.configuration.md#ini.oci8.max-persistent)
-   [oci8.persistent\_timeout](oci8.configuration.md#ini.oci8.persistent-timeout)
-   [oci8.ping\_interval](oci8.configuration.md#ini.oci8.ping-interval)
-   [oci8.prefetch\_lob\_size](oci8.configuration.md#ini.oci8.prefetch-lob-size)
-   [oci8.privileged\_connect](oci8.configuration.md#ini.oci8.privileged-connect)
-   [oci8.statement\_cache\_size](oci8.configuration.md#ini.oci8.statement-cache-size)
-   [odbc.allow\_persistent](odbc.configuration.md#ini.uodbc.allow-persistent)
-   [odbc.check\_persistent](odbc.configuration.md#ini.uodbc.check-persistent)
-   [odbc.max\_persistent](odbc.configuration.md#ini.uodbc.max-persistent)
-   [odbc.max\_links](odbc.configuration.md#ini.uodbc.max-links)
-   [odbc.defaultbinmode](odbc.configuration.md#ini.uodbc.defaultbinmode)
-   [odbc.default\_cursortype](odbc.configuration.md#ini.uodbc.defaultcursortype)
-   [odbc.defaultlrl](odbc.configuration.md#ini.uodbc.defaultlrl)
-   [opcache.consistency\_checks](opcache.configuration.md#ini.opcache.consistency-checks)
-   [opcache.file\_update\_protection](opcache.configuration.md#ini.opcache.file_update_protection)
-   [opcache.force\_restart\_timeout](opcache.configuration.md#ini.opcache.force-restart-timeout)
-   [opcache.interned\_strings\_buffer](opcache.configuration.md#ini.opcache.interned-strings-buffer)
-   [opcache.jit\_bisect\_limit](opcache.configuration.md#ini.opcache.jit-bisect-limit)
-   [opcache.jit\_blacklist\_root\_trace](opcache.configuration.md#ini.opcache.jit-blacklist-root-trace)
-   [opcache.jit\_blacklist\_side\_trace](opcache.configuration.md#ini.opcache.jit-blacklist-side-trace)
-   [opcache.jit\_debug](opcache.configuration.md#ini.opcache.jit-debug)
-   [opcache.jit\_hot\_func](opcache.configuration.md#ini.opcache.jit-hot-func)
-   [opcache.jit\_hot\_loop](opcache.configuration.md#ini.opcache.jit-hot-loop)
-   [opcache.jit\_hot\_return](opcache.configuration.md#ini.opcache.jit-hot-return)
-   [opcache.jit\_hot\_side\_exit](opcache.configuration.md#ini.opcache.jit-hot-side-exit)
-   [opcache.jit\_max\_exit\_counters](opcache.configuration.md#ini.opcache.jit-max-exit-counters)
-   [opcache.jit\_max\_loop\_unrolls](opcache.configuration.md#ini.opcache.jit-max-loop-unrolls)
-   [opcache.jit\_max\_polymorphic\_calls](opcache.configuration.md#ini.opcache.jit-max-polymorphic-calls)
-   [opcache.jit\_max\_recursive\_calls](opcache.configuration.md#ini.opcache.jit-max-recursive-calls)
-   [opcache.jit\_max\_recursive\_returns](opcache.configuration.md#ini.opcache.jit-max-recursive-return)
-   [opcache.jit\_max\_root\_traces](opcache.configuration.md#ini.opcache.jit-max-root-traces)
-   [opcache.jit\_max\_side\_traces](opcache.configuration.md#ini.opcache.jit-max-side-traces)
-   [opcache.log\_verbosity\_level](opcache.configuration.md#ini.opcache.log-verbosity-level)
-   [opcache.max\_file\_size](opcache.configuration.md#ini.opcache.max-file-size)
-   [opcache.opt\_debug\_level](opcache.configuration.md#ini.opcache.opt_debug_level)
-   [opcache.optimization\_level](opcache.configuration.md#ini.opcache.optimization-level)
-   [opcache.revalidate\_freq](opcache.configuration.md#ini.opcache.revalidate-freq)
-   [output\_buffering](outcontrol.configuration.md#ini.output-buffering)
-   [pcre.backtrack\_limit](pcre.configuration.md#ini.pcre.backtrack-limit)
-   [pcre.recursion\_limit](pcre.configuration.md#ini.pcre.recursion-limit)
-   [pgsql.max\_links](pgsql.configuration.md#ini.pgsql.max-links)
-   [pgsql.max\_persistent](pgsql.configuration.md#ini.pgsql.max-persistent)
-   [post\_max\_size](ini.core.md#ini.post-max-size)
-   [realpath\_cache\_size](ini.core.md#ini.realpath-cache-size)
-   [realpath\_cache\_ttl](ini.core.md#ini.realpath-cache-ttl)
-   [session.cache\_expire](session.configuration.md#ini.session.cache-expire)
-   [session.cookie\_lifetime](session.configuration.md#ini.session.cookie-lifetime)
-   [session.gc\_divisor](session.configuration.md#ini.session.gc-divisor)
-   [session.gc\_maxlifetime](session.configuration.md#ini.session.gc-maxlifetime)
-   [session.gc\_probability](session.configuration.md#ini.session.gc-probability)
-   [soap.wsdl\_cache\_limit](soap.configuration.md#ini.soap.wsdl-cache-limit)
-   [soap.wsdl\_cache\_ttl](soap.configuration.md#ini.soap.wsdl-cache-ttl)
-   [unserialize\_max\_depth](var.configuration.md#ini.unserialize-max-depth)
-   [upload\_max\_filesize](ini.core.md#ini.upload-max-filesize)
-   [user\_ini.cache\_ttl](ini.core.md#ini.user-ini.cache-ttl)
-   [xmlrpc\_error\_number](errorfunc.configuration.md#ini.xmlrpc-error-number)
-   [zend.assertions](ini.core.md#ini.zend.assertions)
-   [zlib.output\_compression\_level](zlib.configuration.md#ini.zlib.output-compression-level)
