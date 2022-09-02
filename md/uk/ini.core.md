---
navigation:
  - ini.sections.md: « Список розділів php.ini
  - extensions.md: Список/класифікація модулів »
  - index.md: PHP Manual
  - ini.md: Директиви php.ini
title: Опис вбудованих директив php.ini
---
## Опис вбудованих директив php.ini

Цей список включає вбудовані директиви php.ini, які можна використовувати для налаштування PHP. Директиви, які обробляються модулями, перераховані та детально описані на сторінках документацій відповідних модулів. Наприклад, інформацію про директиви сесій можна знайти на [странице документации сессий](session.configuration.md)

> **Зауваження**
> 
> Представлені тут значення за промовчанням використовуються у разі, якщо не було підключено php.ini; значення для бойового php.ini та розробки можуть відрізнятися.

## Мовні опції

**Опції мови та інших налаштувань**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [shortopentag](ini.core.md#ini.short-open-tag) | "1" | PHPINIPERDIR |  |
| [precision](ini.core.md#ini.precision) | "14" | PHPINIALL |  |
| [serializeprecision](ini.core.md#ini.serialize-precision) | "-1" | PHPINIALL | До версії PHP 7.1.0 значення за промовчанням дорівнювало 17. |
| [disablefunctions](ini.core.md#ini.disable-functions) | "" | Тільки PHPINISYSTEM |  |
| [disableclasses](ini.core.md#ini.disable-classes) | "" | Тільки php.ini |  |
| [exitвінtimeout](ini.core.md#ini.exit-on-timeout) | "" | PHPINIALL |  |
| [exposephp](ini.core.md#ini.expose-php) | "1" | Тільки php.ini |  |
| [hardtimeout](ini.core.md#ini.hard-timeout) | "2" | PHPINISYSTEM | Доступна з версії PHP 7.1.0. |
| [zend.exceptionignoreargs](ini.core.md#ini.zend.exception-ignore-args) | "0" | PHPINIALL | Доступна з версії PHP 7.4.0 |
| [zend.multibyte](ini.core.md#ini.zend.multibyte) | "0" | PHPINIALL |  |
| [zend.scriptencoding](ini.core.md#ini.zend.script-encoding) | NULL | PHPINIALL |  |
| [zend.detectunicode](ini.core.md#ini.zend.detect-unicode) | NULL | PHPINIALL |  |
| [zend.signalcheck](ini.core.md#ini.zend.signal-check) | "0" | PHPINISYSTEM |  |
| [zend.assertions](ini.core.md#ini.zend.assertions) | "1" | PHPINIALL з обмеженнями |  |
| [zend.exceptionstringparammaxlen](ini.core.md#ini.zend.exception-string-param-max-len) | "15" | PHPINIALL | Доступно з PHP 8.0.0. |

Коротке пояснення конфігураційних директив.

`short_open_tag` bool

Визначає, чи дозволяється коротка форма запису (**`<? ?>`**) тегів PHP. Якщо ви хочете використовувати PHP спільно з XML, ви можете вимкнути цю опцію, щоб безперешкодно використовувати **`<?xml ?>`**. В іншому випадку, ви можете відобразити це за допомогою PHP, наприклад: **`<?php echo '<?xml version="1.0"?>'; ?>`**. Якщо ж ця опція вимкнена, ви повинні використовувати довгу форму тега PHP (**`<?php ?>`**

> **Зауваження**
> 
> Ця директива не впливає на скорочення **`<?=`**, яка завжди доступна.

`precision` int

Кількість цифр, що відображаються для чисел з плаваючою точкою . `-1` означає, що буде використано вдосконалений алгоритм округлення таких чисел.

`serialize_precision` int

Кількість значущих цифр, що зберігаються при серіалізації чисел з плаваючою точкою . `-1` означає, що буде використано вдосконалений алгоритм округлення таких чисел.

`expose_php` bool

Видає факт присутності PHP на сервері, включаючи передачу версії PHP в заголовку HTTP (наприклад, X-Powered-By: PHP/5.3.7).

`disable_functions` string

Ця директива дозволяє вимкнути деякі функції. Вона приймає список імен функцій, розділений комами.

Тільки [внутрішні функції](functions.internal.md) можуть бути відключені за допомогою цієї директиви . [Функції користувача](functions.user-defined.md) їй не схильні.

Ця директива має бути встановлена ​​у php.ini. Наприклад, її не можна використовувати в httpd.conf.

`disable_classes` string

Ця директива дозволяє вимкнути деякі класи. Вона приймає список імен класів, розділених комами. Ця директива має бути встановлена ​​у php.ini. Наприклад, її не можна використовувати в httpd.conf.

`zend.assertions` int

Якщо встановлено значення `1`, код перевірки буде виконуватися (режим розробки). Якщо заданий `0`, код перевірок буде згенерований, однак виконуватися не буде. Якщо поставлено `-1`, код перевірки не буде генеруватися (продуктивний режим).

> **Зауваження**
> 
> Якщо процес стартований у режимі релізу, [zend.assertions](ini.core.md#ini.zend.assertions) не може бути змінений під час виконання, оскільки код тверджень не генерується.
> 
> Якщо процес стартований у режимі розробки, [zend.assertions](ini.core.md#ini.zend.assertions) не може бути виставлений у `-1` під час виконання..

`zend.exception_string_param_max_len` int

Максимальна довжина аргументів рядкової функції рядкових трасування стека. Значення має бути в діапазоні від `"0"` до `"1000000"`

`hard_timeout` int

Коли закінчується час очікування, встановлений у [maxexecutiontime](info.configuration.md#ini.max-execution-time), середовище виконання PHP акуратно відключить ресурси. Якщо під час цього щось застрягне, час очікування буде встановлено на вказану кількість секунд. Коли закінчиться жорсткий час очікування, PHP завершить роботу з помилкою. Якщо встановлено значення 0, жорсткий час очікування ніколи не активується.

Коли PHP зупиняється після жорсткого часу очікування, це буде виглядати приблизно так:

```
Fatal error: Maximum execution time of 30+2 seconds exceeded (terminated) in Unknown on line 0
```

`zend.exception_ignore_args` bool

Виключає аргументи трасування стека, згенерованих з винятків.

`zend.multibyte` bool

Дозволяє парсинг вихідних файлів у багатобайтні кодування. Включення zend.multibyte потрібно для використання кодувань символів подібних до SJIS, BIG5 і т.д., що містять спеціальні символи в багатобайтних рядкових даних. Сумісні з ISO-8859-1 кодування, наприклад UTF-8, EUC тощо, не потребують цієї опції.

Модуль zend.multibyte вимагає модуля "mbstring".

`zend.script_encoding` string

Це значення буде використано лише за відсутності директиви [declare(encoding=...)](control-structures.declare.md#control-structures.declare.encoding) на початку скрипту. При використанні несумісних кодувань з ISO-8859-1, потрібно використовувати опції і zend.multibyte і zend.scriptencoding.

Літеральні рядки мають бути транслітеровані із zend.scriptencoding у mbstring.internalencoding, якби викликали [мбconvertencoding()](function.mb-convert-encoding.md)

`zend.detect_unicode` bool

Визначає, чи потрібно перевіряти BOM (Byte Order Mark, мітка порядку байт) та коректність багатобайтних символів у файлі. Ця перевірка здійснюється до дзвінка [haltcompiler()](function.halt-compiler.md). Доступна лише у режимі Zend Multibyte.

`zend.signal_check` bool

Визначає, чи потрібно перевіряти замінені обробники сигналів після завершення скрипта.

`exit_on_timeout` bool

Ця директива є тільки для Apache1 modphp, яка змушує нащадка Apache завершитись, якщо перевищено час очікування виконання скрипту PHP. Перевищення часу очікування призводить до внутрішнього виклику longjmp() Apache1, який залишає деякі модулі в неузгодженому стані. Після завершення процесу всі незняті блокування або пам'ять буде очищено.

## Обмеження ресурсів

**Обмеження ресурсів**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [memorylimit](ini.core.md#ini.memory-limit) | "128M" | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`memory_limit` int

Ця директива визначає максимальний обсяг пам'яті в байтах, який дозволяється використовувати скрипту. Це допомагає запобігти ситуації, коли погано написаний скрипт з'їдає всю доступну пам'ять сервера. Для того, щоб усунути обмеження, встановіть значення цієї директиви в `-1`

Якщо використовується int значення вимірюється байтами. Ви також можете використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes)

Дивіться також: [maxexecutiontime](info.configuration.md#ini.max-execution-time)

## Налаштування продуктивності

**Налаштування продуктивності**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [realpathcachesize](ini.core.md#ini.realpath-cache-size) | "ЧМ" | PHPINISYSTEM | До PHP 7.0.16 та 7.1.2, за умовчанням було `"16K"` |
| [realpathcachettl](ini.core.md#ini.realpath-cache-ttl) | "120" | PHPINISYSTEM |  |

> **Зауваження**
> 
> Використання [openbasedir](ini.core.md#ini.open-basedir) *відключить* кеш realpath.

Коротке пояснення конфігураційних директив.

`realpath_cache_size` int

Визначає розмір кешу realpath, що використовується в PHP. Це значення має бути збільшено на системах, в яких PHP відкриває велику кількість файлів відповідно до кількості виконуваних файлових операцій.

Розмір рівний загальному числу байт, що зберігається в рядках шляхів, плюс розмір даних пов'язаних з елементом, що кешується. Це означає, що для зберігання довгих шляхів у кеші, розмір цього кешу має бути більшим. Це значення не визначає безпосередньо кількість різних шляхів, які можуть бути закешовані.

Розмір, необхідний кешування, залежить від системи.

`realpath_cache_ttl` int

Час (в секундах) протягом якого буде використаний кеш realpath для зазначеного файлу або директорії. Для систем з файлами, що рідко змінюються, це значення можна збільшити.

## Обробка даних

**Конфігураційні опції обробки даних**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [argseparator.output](ini.core.md#ini.arg-separator.output) | "&" | PHPINIALL |  |
| [argseparator.input](ini.core.md#ini.arg-separator.input) | "&" | PHPINIPERDIR |  |
| [variablesorder](ini.core.md#ini.variables-order) | "EGPCS" | PHPINIPERDIR |  |
| [requestorder](ini.core.md#ini.request-order) | "" | PHPINIPERDIR |  |
| [autoglobalsjit](ini.core.md#ini.auto-globals-jit) | "1" | PHPINIPERDIR |  |
| [registerargcargv](ini.core.md#ini.register-argc-argv) | "1" | PHPINIPERDIR |  |
| [enablepostdatareading](ini.core.md#ini.enable-post-data-reading) | "1" | PHPINIPERDIR |  |
| [postmaxsize](ini.core.md#ini.post-max-size) | "8M" | PHPINIPERDIR |  |
| [autoprependfile](ini.core.md#ini.auto-prepend-file) | NULL | PHPINIPERDIR |  |
| [autoappendfile](ini.core.md#ini.auto-append-file) | NULL | PHPINIPERDIR |  |
| [defaultmimetype](ini.core.md#ini.default-mimetype) | "text/html" | PHPINIALL |  |
| [defaultcharset](ini.core.md#ini.default-charset) | "UTF-8" | PHPINIALL |  |
| [inputencoding](ini.core.md#ini.input-encoding) | "" | PHPINIALL |  |
| [outputencoding](ini.core.md#ini.output-encoding) | "" | PHPINIALL |  |
| [internalencoding](ini.core.md#ini.internal-encoding) | "" | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`arg_separator.output` string

Цей роздільник використовується в генерованих PHP URL як роздільник аргументів.

`arg_separator.input` string

Список роздільників, що використовуються PHP для отримання змінних із URL.

> **Зауваження**
> 
> Кожен символ у цій директиві вважається роздільником!

`variables_order` string

Встановлює порядок обробки змінних EGPCS (`E`nvironment, `G`et, `P`ost, `C`ookie, та `S`server). Наприклад, якщо variablesorder встановлена ​​в `"SP"`, то PHP створить [superglobals](language.variables.predefined.md) [SERVER](reserved.variables.server.md) і [POST](reserved.variables.post.md), але не буде створювати [ENV](reserved.variables.environment.md) [GET](reserved.variables.get.md) і [COOKIE](reserved.variables.cookies.md). Установка в "" означає, що жодна [superglobals](language.variables.predefined.md) не буде встановлено.

**Увага**

У CGI та FastCGI SAPI, [SERVER](reserved.variables.server.md) також додаються значення змінних оточення; `S` завжди еквівалентна `ES` незалежно від положення `E` у цій директиві.

> **Зауваження**
> 
> Ця директива також впливає на вміст та порядок змінної [REQUEST](reserved.variables.request.md)

`request_order` string

Ця директива регулює порядок, в якому PHP додає змінні GET, POST та Cookie до масиву. REQUEST. Додавання проводиться ліворуч, нові значення перезаписують старі.

Якщо значення цієї директиви не встановлено, використовується значення директиви [variablesorder](ini.core.md#ini.variables-order) для вмісту змінної [REQUEST](reserved.variables.request.md)

Врахуйте, що файли php.ini, що постачаються з дистрибутивом, з міркувань безпеки не містять значення `'C'` (Cookies).

`auto_globals_jit` bool

Коли увімкнено, змінні SERVER, REQUEST та ENV створюються в той момент, коли вони вперше використовуються (Just In Time), а не на початку виконання скрипту. Якщо ці змінні у скрипті не використовуються, включення цієї директиви призведе до зростання продуктивності.

**Увага**

Використання змінних SERVER, REQUEST та ENV перевіряється на стадії компіляції, тому їх використання за допомогою, наприклад, [змінних змінних](language.variables.variable.md) не запустить їхньої ініціалізації.

`register_argc_argv` bool

Повідомляє PHP, чи слід оголошувати змінні argv та argc (які міститимуть GET-інформацію). Дивіться також [Використання PHP у командному рядку](features.commandline.md)

`enable_post_data_reading` bool

При відключенні цієї опції суперглобальні змінні [POST](reserved.variables.post.md) і [FILES](reserved.variables.files.md) *не будуть* заповнюватись. Єдиним способом прочитати POST-дані буде читання обгортки потоку [php://input](wrappers.php.md). Це може бути корисним при проксуванні запитів або обробки POST-даних способом, що більш ефективно використовує пам'ять.

`post_max_size` int

Встановлює максимально допустимий розмір даних, які надсилаються методом POST. Це також впливає на завантаження файлів. Для завантаження великих файлів це значення має бути більшим за значення директиви [uploadmaxfilesize](ini.core.md#ini.upload-max-filesize). В сутності, [memorylimit](ini.core.md#ini.memory-limit) має бути більше ніж `post_max_size`. Якщо використовується int значення вимірюється байтами. Ви також можете використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes). Якщо розмір POST даних більше ніж postmaxsize, [суперглобальні змінні](language.variables.superglobals.md) [POST](reserved.variables.post.md) і [FILES](reserved.variables.files.md) будуть порожніми. Це можна відстежити у різний спосіб, наприклад передавши [GET](reserved.variables.get.md) змінну скрипт, який обробляє дані, тобто . `<form action="edit.php?processed=1">`, а потім перевірити, чи встановлена ​​змінна [GET\['processed'\]](reserved.variables.get.md)

> **Зауваження**
> 
> PHP дозволяє скорочення значень байт, включаючи K (кіло), M (мега) та G (гіга). PHP автоматично перетворює всі ці скорочення. Будьте обережні з перевищенням діапазону 32-бітових цілих значень (якщо ви використовуєте 32-бітну версію), оскільки це призведе до помилки вашого скрипту.

**список змін `post_max_size`**

| Версия | Описание |
| --- | --- |
|  | Встановлення `post_max_size` = 0 не знімає обмеження, якщо контент має тип application/x-www-form-urlencoded або не зареєстрований у PHP. |
|  | Стало можливим зняти обмеження на розмір пост-запиту установкою `post_max_size` 0. |

`auto_prepend_file` string

Визначає ім'я файлу, який автоматично оброблятиметься перед основним файлом. Файл викликається так, ніби він був підключений за допомогою функції [require](function.require.md), так що [includepath](ini.core.md#ini.include-path) також використовується.

Спеціальне значення `none` відключає цю директиву.

`auto_append_file` string

Визначає ім'я файлу, який автоматично оброблятиметься після основного файлу. Файл викликається так, ніби він був підключений за допомогою функції [require](function.require.md), так що [includepath](ini.core.md#ini.include-path) також використовується.

Спеціальне значення `none` відключає цю директиву.

> **Зауваження**: Якщо скрипт завершує роботу за допомогою [exit()](function.exit.md), auto-append *НЕ* виконується.

`default_mimetype` string

За промовчанням PHP виводить назву кодування в заголовку Content-Type. Якщо не потрібно передавати кодування, просто залиште цю опцію порожньою.

"media type" за замовчуванням встановлено як "text/html".

`default_charset` string

"UTF-8" є значенням за промовчанням і використовується як кодування за промовчанням для функцій [htmlentities()](function.htmlentities.md) [htmlentitydecode()](function.html-entity-decode.md) і [htmlspecialchars()](function.htmlspecialchars.md), якщо параметр `encoding` не вказано. Значення `default_charset` також використовується для вказівки кодування за промовчанням для функцій [iconv](book.iconv.md), якщо конфігураційні опції [`iconv.input_encoding`](iconv.configuration.md#ini.iconv.input-encoding) [`iconv.output_encoding`](iconv.configuration.md#ini.iconv.output-encoding) і [`iconv.internal_encoding`](iconv.configuration.md#ini.iconv.internal-encoding) не встановлені, і для функцій [mbstring](book.mbstring.md), якщо не встановлено [`mbstring.http_input`](mbstring.configuration.md#ini.mbstring.http-input) [`mbstring.http_output`](mbstring.configuration.md#ini.mbstring.http-output) [`mbstring.internal_encoding`](mbstring.configuration.md#ini.mbstring.internal-encoding)

Усі версії PHP використовують це значення як кодування для стандартного заголовка Content-Type, що надсилається PHP, якщо цей заголовок не перевизначений викликом функції [header()](function.header.md)

Не рекомендується встановлювати `default_charset` у порожнє значення.

`input_encoding` string

Ця опція використовується для багатобайтних модулів, таких як mbstring та iconv. За промовчанням порожньо.

`output_encoding` string

Ця опція використовується для багатобайтних модулів, таких як mbstring та iconv. За промовчанням порожньо.

`internal_encoding` string

Ця опція використовується для багатобайтних модулів, таких як mbstring та iconv. За промовчанням порожньо. У цьому випадку використовується [defaultcharset](ini.core.md#ini.default-charset)

## Шляхи та Директорії

**Конфігураційні Опції Шляхів та Директорій**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [includepath](ini.core.md#ini.include-path) | ".;/path/to/php/pear" | PHPINIALL |  |
| [openbasedir](ini.core.md#ini.open-basedir) | NULL | PHPINIALL |  |
| [docroot](ini.core.md#ini.doc-root) | NULL | PHPINISYSTEM |  |
| [userdir](ini.core.md#ini.user-dir) | NULL | PHPINISYSTEM |  |
| [userini.cachettl](ini.core.md#ini.user-ini.cache-ttl) | "300" | PHPINISYSTEM |  |
| [userini.filename](ini.core.md#ini.user-ini.filename) | ".user.ini" | PHPINISYSTEM |  |
| [extensiondir](ini.core.md#ini.extension-dir) | "/path/to/php" | PHPINISYSTEM |  |
| [extension](ini.core.md#ini.extension) | NULL | Тільки php.ini |  |
| [zendextension](ini.core.md#ini.zend-extension) | NULL | Тільки php.ini |  |
| [cgi.checkshebangline](ini.core.md#ini.cgi.check-shebang-line) | "1" | PHPINISYSTEM |  |
| [cgi.discardpath](ini.core.md#ini.cgi.discard-path) | "0" | PHPINISYSTEM |  |
| [cgi.fixpathinfo](ini.core.md#ini.cgi.fix-pathinfo) | "1" | PHPINISYSTEM |  |
| [cgi.forceredirect](ini.core.md#ini.cgi.force-redirect) | "1" | PHPINISYSTEM |  |
| [cgi.nph](ini.core.md#ini.cgi.nph) | "0" | PHPINISYSTEM |  |
| [cgi.redirectstatusenv](ini.core.md#ini.cgi.redirect-status-env) | NULL | PHPINISYSTEM |  |
| [cgi.rfc2616headers](ini.core.md#ini.cgi.rfc2616-headers) | "0" | PHPINIALL |  |
| [fastcgi.impersonate](ini.core.md#ini.fastcgi.impersonate) | "0" | PHPINISYSTEM |  |
| [fastcgi.logging](ini.core.md#ini.fastcgi.logging) | "1" | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`include_path` string

Вказує список директорій, у яких функції [require](function.require.md) [include](function.include.md) [fopen()](function.fopen.md) [file()](function.file.md) [readfile()](function.readfile.md) і [filegetcontents()](function.file-get-contents.md) шукають файли Формат відповідає формату системної змінної оточення PATH: список директорій, розділених двокрапкою в Unix або крапкою з комою у Windows.

При пошуку файлів, що підключаються, PHP окремо розглядає кожне значення в includepath. Він перевіряє перший шлях, якщо файл в ньому не знайдений, то він переходить до наступного, і так до тих пір, поки не знайде файл, що підключається, або поверне **`E_WARNING`** або **`E_ERROR`**. Ви можете змінити ваш includepath під час виконання скрипту за допомогою функції [setincludepath()](function.set-include-path.md)

**Приклад #1 includepath в Unix**

includepath=".:/php/includes"

**Приклад #2 includepath у Windows**

includepath=".;c:phpincludes"

Використання `.` у includepath дозволяє задавати відносні шляхи для підключення файлів, оскільки точка означає поточну директорію. Однак, більш ефективно використовувати `include './file'`чим змушувати PHP щоразу перевіряти поточну директорію при підключенні кожного файлу.

> **Зауваження**
> 
> Змінні оточення (`ENV`) також доступні в .ini файлах. Таким чином, можна посилатися на домашню директорію за допомогою директив `${LOGIN}` і `${USER}`
> 
> Змінні оточення можуть відрізнятися між різними серверними API, оскільки самі оточення відрізняються один від одного.

**Приклад #3 Налаштування includepath за допомогою змінної оточення ${USER} в Unix**

includepath = ".:${USER}/pear/php"

`open_basedir` string

Обмежує вказаним деревом каталогів файли, які можуть бути доступні для PHP, включаючи файл. Ця директива *НЕ* піддається впливу безпечного режиму.

Коли скрипт намагається отримати доступ до файлу, наприклад, за допомогою функції [fopen()](function.fopen.md) або [gzopen()](function.gzopen.md), перевіряється місцезнаходження файлу. Якщо файл знаходиться поза вказаним деревом каталогів, PHP відмовиться його відкривати. Всі символічні посилання будуть розкриті, так що за їх допомогою не вдасться обійти це обмеження. Якщо файл не існує, то символічне посилання не може бути прочитане і ім'я файлу (прочитане) буде розглядатися **openbasedir**

Опція **openbasedir** може поширюватися як на функції до роботи з файлової системою; наприклад, якщо `MySQL` налаштований використовувати драйвер `mysqlnd`, то `LOAD DATA INFILE` підпадає під опцію **openbasedir**. Безліч функцій PHP також використовує `open_basedir`

Спеціальне значення `.` позначає, що робоча директорія скрипта буде використана як базова директорія. Однак це трохи небезпечно, так як поточна директорія скрипту може бути легко змінена за допомогою [chdir()](function.chdir.md)

У httpd.conf, **openbasedir** може бути вимкнена (наприклад, для деяких віртуальних хостів) [тим же способом](configuration.changes.md#configuration.changes.apache), як і будь-яка інша конфігураційна директива: "`php_admin_value open_basedir none`".

У Windows розділяйте каталоги крапкою з комою. На всіх інших системах, розділяйте директорії двокрапкою. При роботі в якості модуля Apache, шляхи **openbasedir** автоматично успадковуються від батьківських директорій.

Обмеження, що визначається **openbasedir** є ім'ям директорії, а чи не префіксом.

За промовчанням всі файли можуть бути відкриті.

> **Зауваження**
> 
> Значення openBasedir можна зробити суворішим під час виконання скрипта. Це означає, що якщо openbasedir була встановлена ​​в `/www/` в php.ini, то скрипт може утиснути конфігурацію до `/www/tmp/` під час виконання за допомогою [iniset()](function.ini-set.md). При вказівці кількох директорій можна використовувати константу **`PATH_SEPARATOR`** як роздільник шляхів, який залежить від операційної системи.

> **Зауваження**
> 
> Використання опції openbasedir встановить [realpathcachesize](ini.core.md#ini.realpath-cache-size) на значення `0` і таким чином *відключить* кеш realpath.

**Застереження**

`open_basedir` - це просто додаткове підстрахування, яке аж ніяк не є всеосяжним і тому на нього не можна покладатися, коли йдеться про безпеку.

`doc_root` string

Коренева директорія PHP на цьому сервері. Використовується лише у випадку, якщо не пуста. Якщо PHP не був скомпільований з FORCEREDIRECT, вам *слід* встановити docroot, якщо ви використовуєте PHP як CGI під будь-яким веб-сервером (крім IIS). Альтернативою є використання конфігураційної директиви [cgi.forceredirect](ini.core.md#ini.cgi.force-redirect), Мова про яку йде нижче.

`user_ini.cache_ttl` int

`user_ini.filename` string

`user_dir` string

Базове ім'я директорії, що використовується в домашньому каталозі користувача для файлів PHP, наприклад, publichtml.

`extension_dir` string

У якій директорії PHP повинен шукати модулі, що динамічно завантажуються. Рекомендується вказувати абсолютний шлях. Дивіться також: [enableдл](info.configuration.md#ini.enable-dl) і [dl()](function.dl.md)

`extension` string

Які модулі, що динамічно завантажуються, повинні бути завантажені при старті PHP.

`zend_extension` string

Ім'я модуля Zend (наприклад, XDebug), що динамічно завантажується, який повинен бути завантажений при старті PHP.

`cgi.check_shebang_line` bool

Контролює, чи потрібно перевіряти перший рядок CGI PHP-скрипту на зміст `#!` (Shebang). Цей рядок може бути необхідним, якщо скрипт повинен підтримувати як окремий запуск, так і за допомогою PHP CGI. PHP у режимі CGI пропускає цей рядок і ігнорує його вміст, якщо ця директива включена.

`cgi.discard_path` bool

Якщо дозволено, бінарний файл PHP CGI може безпечно розташовуватися поза веб-деревом і люди не зможуть обійти безпеку .htaccess.

`cgi.fix_pathinfo` bool

Забезпечує підтримку *правильних* `PATH_INFO``PATH_TRANSLATED` у CGI. Раніше PHP просто встановлював `PATH_TRANSLATED` в `SCRIPT_FILENAME` і не звертав уваги на `PATH_INFO`. Для отримання додаткової інформації про `PATH_INFO`зверніться до специфікації CGI. Встановлення цього значення `1` змусить PHP CGI виправляти свій шлях відповідно до специфікації. Значення 0 відповідає попередньому поведінці. За замовчуванням опція увімкнена. Ви повинні виправити свої скрипти так, щоб вони використовували `SCRIPT_FILENAME` замість `PATH_TRANSLATED`

`cgi.force_redirect` bool

Директива cgi.forceredirect необхідна для забезпечення безпеки під час роботи PHP як CGI під більшістю веб-серверів. Якщо залишити її невизначеною, PHP за промовчанням включає цю директиву. Ви можете вимкнути її *на свій страх і ризик*

> **Зауваження**
> 
> Користувачам Windows: У разі використання IIS ця опція *повинна* бути вимкнена. Те саме необхідно для OmniHTTPD і Xitami.

`cgi.nph` bool

Якщо cgi.nph дозволена, cgi примусово повертатиме код 200 на кожен запит.

`cgi.redirect_status_env` string

Якщо cgi.forceredirect включено і ви працюєте не під веб-сервером Apache або Netscape (iPlanet), вам *може* знадобиться встановити змінну оточення, яку шукатиме PHP щоб переконатися, що він може продовжувати виконання.

> **Зауваження**
> 
> Встановлення цієї змінної *може* спричинити проблеми з безпекою, так що *ви повинні знати, що ви робите*

`cgi.rfc2616_headers` int

Повідомляє PHP, який тип заголовків використовувати при надсиланні коду відповіді HTTP. Якщо встановлено 0, PHP відправляє [» RFC 3875](http://www.faqs.org/rfcs/rfc3875) заголовок "Status:", який підтримується Apache та іншими веб-серверами. Якщо встановлено в 1, PHP надсилає заголовки, відповідні [» RFC 2616](http://www.faqs.org/rfcs/rfc2616)

Якщо ця опція включена і ви використовуєте PHP в оточенні CGI (наприклад, PHP-FPM), замість використання HTTP-заголовків відповіді в стилі RFC 2616, потрібно використовувати їх еквівалент зі стандарту RFC 3875, наприклад, замість header("HTTP/1.0 404 Not found"); потрібно використовувати header("Status: 404 Not Found");

Залиште значення 0, якщо ви не впевнені в тому, що це означає.

`fastcgi.impersonate` string

FastCGI під IIS (в ОС на базі WINNT) підтримує можливість імперсонації прав безпеки клієнта, що викликає. Це дозволяє IIS визначити контекст безпеки, у якому виконується запит. modfastcgi під Apache на даний момент не підтримує цю можливість (03/17/2002). Встановіть 1 під час роботи під IIS. Значення за замовчуванням – нуль.

`fastcgi.logging` bool

Включає логування SAPI під час використання FastCGI. Логування увімкнено за замовчуванням.

## Закачування файлів

**Конфігураційні Опції Закачування файлів**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [fileuploads](ini.core.md#ini.file-uploads) | "1" | PHPINISYSTEM |  |
| [uploadtmpdir](ini.core.md#ini.upload-tmp-dir) | NULL | PHPINISYSTEM |  |
| [maxinputnestinglevel](info.configuration.md#ini.max-input-nesting-level) |  | PHPINIPERDIR |  |
| [maxinputvars](info.configuration.md#ini.max-input-vars) |  | PHPINIPERDIR |  |
| [uploadmaxfilesize](ini.core.md#ini.upload-max-filesize) | "2M" | PHPINIPERDIR |  |
| [maxfileuploads](ini.core.md#ini.max-file-uploads) |  | PHPINIPERDIR |  |

Коротке пояснення конфігураційних директив.

`file_uploads` bool

Дозволяти чи не дозволяти [закачивание файлов](features.file-upload.md). Дивіться також директиви [uploadmaxfilesize](ini.core.md#ini.upload-max-filesize) [uploadtmpdir](ini.core.md#ini.upload-tmp-dir) і [postmaxsize](ini.core.md#ini.post-max-size)

`upload_tmp_dir` string

Тимчасова директорія, що використовується для зберігання файлів під час закачування. Має бути доступною для запису користувачеві, від імені якого запущено PHP. Якщо не вказано, використовується каталог за промовчанням для вашої системи.

Якщо до зазначеної директорії немає прав на запис, PHP відкотиться назад до системної тимчасової директорії, яка використовується за умовчанням. Якщо увімкнено директиву [openbasedir](ini.core.md#ini.open-basedir), то для успішного завантаження файлів системна директорія за умовчанням має бути дозволена.

`upload_max_filesize` int

Максимальний розмір файлу, що закачується.

[postmaxsize](ini.core.md#ini.post-max-size) має бути більше, ніж це значення.

Якщо використовується int значення вимірюється байтами. Ви також можете використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes)

`max_file_uploads` int

Максимально дозволена кількість файлів, що одночасно закачуються. Порожні поля завантаження не розглядаються цим обмеженням.

## Загальний SQL

**Конфігураційні Опції Загального SQL**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [sql.safemode](ini.core.md#ini.sql.safe-mode) | "0" | PHPINISYSTEM | Видалено в PHP 7.2.0 |

Коротке пояснення конфігураційних директив.

`sql.safe_mode` bool

Якщо увімкнено, функції з'єднання з базою даних, що використовують значення за замовчуванням, будуть використовувати ці значення замість будь-яких аргументів, що передаються. Для значень за замовчуванням дивіться документацію щодо функцій підключення відповідної бази даних.

**Увага**

Ця опція *ВИДАЛЕНО* у PHP 7.2.0.

## Особливі налаштування для Windows

**Особливі опції конфігурації для Windows**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [windows.showcrtwarning](ini.core.md#ini.windows-show-crt-warning) | "0" | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`windows.show_crt_warning` bool

При ввімкненні цієї директиви буде відображено попередження Windows CRT.
