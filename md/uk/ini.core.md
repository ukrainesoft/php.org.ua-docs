---
navigation:
  - ini.sections.md: « Список розділів php.ini
  - extensions.md: Список/класифікація модулів »
  - index.md: PHP Manual
  - ini.md: Директиви php.ini
title: Опис вбудованих директив php.ini
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Опис вбудованих директив php.ini

Цей список включає вбудовані директиви php.ini, які можна використовувати для налаштування PHP. Директиви, які обробляються модулями, перераховані та детально описані на сторінках документацій відповідних модулів. Наприклад, інформацію про директиви сесій можна знайти на [сторінці документації сесій](session.configuration.md)

> **Зауваження** :
> 
> Представлені тут значення за замовчуванням використовуються у випадку, якщо не було підключено php.ini; значення для бойового php.ini та розробки можуть відрізнятися.

## Мовні опції

**Опції мови та інших налаштувань**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [short\_open\_tag](ini.core.md#ini.short-open-tag) | "1" | **`INI_PERDIR`** |  |
| [precision](ini.core.md#ini.precision) | "14" | **`INI_ALL`** |  |
| [serialize\_precision](ini.core.md#ini.serialize-precision) | "-1" | **`INI_ALL`** | До версії PHP 7.1.0 значення за промовчанням дорівнювало 17. |
| [disable\_functions](ini.core.md#ini.disable-functions) | "" | Тільки **`INI_SYSTEM`** |  |
| [disable\_classes](ini.core.md#ini.disable-classes) | "" | Тільки php.ini |  |
| [exit\_on\_timeout](ini.core.md#ini.exit-on-timeout) | "" | **`INI_ALL`** |  |
| [expose\_php](ini.core.md#ini.expose-php) | "1" | Тільки php.ini |  |
| [hard\_timeout](ini.core.md#ini.hard-timeout) | "2" | **`INI_SYSTEM`** | Доступна з версії PHP 7.1.0. |
| [zend.exception\_ignore\_args](ini.core.md#ini.zend.exception-ignore-args) | "0" | **`INI_ALL`** | Доступна з версії PHP 7.4.0 |
| [zend.multibyte](ini.core.md#ini.zend.multibyte) | "0" | **`INI_ALL`** |  |
| [zend.script\_encoding](ini.core.md#ini.zend.script-encoding) | NULL | **`INI_ALL`** |  |
| [zend.detect\_unicode](ini.core.md#ini.zend.detect-unicode) | NULL | **`INI_ALL`** |  |
| [zend.signal\_check](ini.core.md#ini.zend.signal-check) | "0" | **`INI_SYSTEM`** |  |
| [zend.assertions](ini.core.md#ini.zend.assertions) | "1" | **`INI_ALL`** з обмеженнями |  |
| [zend.exception\_string\_param\_max\_len](ini.core.md#ini.zend.exception-string-param-max-len) | "15" | **`INI_ALL`** | Доступно з PHP 8.0.0. |

Коротке пояснення конфігураційних директив.

`short_open_tag`bool

Визначає, чи дозволяється коротка форма запису (**`<? ?>`**) тегів PHP. Якщо ви хочете використовувати PHP спільно з XML, ви можете вимкнути цю опцію, щоб безперешкодно використовувати **`<?xml ?>`**. В іншому випадку, ви можете відобразити це за допомогою PHP, наприклад: **`<?php echo '<?xml version="1.0"?>'; ?>`**. Якщо ж ця опція відключена, ви повинні використовувати довгу форму тега PHP (**`<?php ?>`**

> **Зауваження** :
> 
> Ця директива не впливає на скорочення **`<?=`**, яка завжди доступна.

`precision`int

Кількість цифр, що відображаються для чисел з плаваючою точкою . `-1` означає, що буде використано вдосконалений алгоритм округлення таких чисел.

`serialize_precision`int

Кількість значущих цифр, що зберігаються при серіалізації чисел з плаваючою точкою . `-1` означає, що буде використано вдосконалений алгоритм округлення таких чисел.

`expose_php`bool

Видає факт присутності PHP на сервері, включаючи передачу версії PHP в заголовку HTTP (наприклад, X-Powered-By: PHP/5.3.7).

`disable_functions`string

Ця директива дозволяє вимкнути деякі функції. Вона приймає список імен функцій, розділений комами.

Тільки [внутрішні функції](functions.internal.md) можуть бути відключені за допомогою цієї директиви . [Функції користувача](functions.user-defined.md) їй не схильні.

Ця директива має бути встановлена ​​у php.ini. Наприклад, її не можна використовувати в httpd.conf.

`disable_classes`string

Ця директива дозволяє вимкнути деякі класи. Вона приймає список імен класів, розділених комами. Ця директива має бути встановлена ​​у php.ini. Наприклад, її не можна використовувати в httpd.conf.

`zend.assertions`int

Если задано значение , код перевірки буде виконуватися (режим розробки). Якщо заданий , код перевірок буде згенерований, однак виконуватися не буде. Якщо поставлено `-1`, код перевірки не буде генеруватися (продуктивний режим).

> **Зауваження** :
> 
> Если процесс запущен в режиме релиза,[zend.assertions](ini.core.md#ini.zend.assertions) не може бути змінений під час виконання, оскільки код тверджень не генерується.
> 
> Если процесс запущен в режиме разработки,[zend.assertions](ini.core.md#ini.zend.assertions) не може бути виставлений у `-1` під час виконання..

`zend.exception_string_param_max_len`int

Максимальна довжина аргументів рядкової функції у рядкових трасуваннях стека. Значення має бути в діапазоні від `"0"`до`"1000000"`

`hard_timeout`int

Коли мине час очікування, встановлений у [max\_execution\_time](info.configuration.md#ini.max-execution-time), середовище виконання PHP акуратно відключить ресурси. Якщо під час цього щось застрягне, час очікування буде встановлено на вказану кількість секунд. Коли закінчиться жорсткий час очікування, PHP завершить роботу з помилкою. Якщо встановлено значення 0, жорсткий час очікування ніколи не активується.

Коли PHP зупиняється після жорсткого часу очікування, це буде виглядати приблизно так:

```
Fatal error: Maximum execution time of 30+2 seconds exceeded (terminated) in Unknown on line 0
```

`zend.exception_ignore_args`bool

Виключає аргументи трасування стека, згенерованих з винятків.

`zend.multibyte`bool

Дозволяє парсинг вихідних файлів у багатобайтні кодування. Включення zend.multibyte потрібно для використання кодувань символів подібних до SJIS, BIG5 і т.д., що містять спеціальні символи в багатобайтних рядкових даних. Сумісні з ISO-8859-1 кодування, наприклад UTF-8, EUC тощо, не потребують цієї опції.

Модуль zend.multibyte вимагає модуля "mbstring".

`zend.script_encoding`string

Це значення буде використано лише за відсутності директиви [declare(encoding=...)](control-structures.declare.md#control-structures.declare.encoding) на початку скрипту. При використанні несумісних кодувань з ISO-8859-1, потрібно використовувати опції і zend.multibyte і zend.script\_encoding.

Літеральні рядки мають бути транслітеровані із zend.script\_encoding у mbstring.internal\_encoding, якби викликали [mb\_convert\_encoding()](function.mb-convert-encoding.md)

`zend.detect_unicode`bool

Визначає, чи потрібно перевіряти BOM (Byte Order Mark, мітка порядку байт) та коректність багатобайтних символів у файлі. Ця перевірка здійснюється до дзвінка [\_\_halt\_compiler()](function.halt-compiler.md). Доступна лише у режимі Zend Multibyte.

`zend.signal_check`bool

Визначає, чи потрібно перевіряти замінені обробники сигналів після завершення скрипта.

`exit_on_timeout`bool

Ця директива є тільки для Apache1 mod\_php, яка змушує нащадка Apache завершитись, якщо перевищено час очікування виконання скрипту PHP. Перевищення часу очікування призводить до внутрішнього виклику longjmp() Apache1, який залишає деякі модулі в неузгодженому стані. Після завершення процесу всі незняті блокування або пам'ять буде очищено.

## Обмеження ресурсів

**Обмеження ресурсів**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [memory\_limit](ini.core.md#ini.memory-limit) | "128M" | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`memory_limit`int

Ця директива визначає максимальний обсяг пам'яті в байтах, який дозволяється використовувати скрипту. Це допомагає запобігти ситуації, коли погано написаний скрипт з'їдає всю доступну пам'ять сервера. Для того, щоб усунути обмеження, встановіть значення цієї директиви в `-1`

Якщо вказано ціле значення (int), обсяг вимірюється байтами. Можна також використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes)

Смотрите также:[max\_execution\_time](info.configuration.md#ini.max-execution-time)

## Налаштування продуктивності

**Налаштування продуктивності**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [realpath\_cache\_size](ini.core.md#ini.realpath-cache-size) | "4M" | **`INI_SYSTEM`** | До PHP 7.0.16 та 7.1.2, за умовчанням було `"16K"` |
| [realpath\_cache\_ttl](ini.core.md#ini.realpath-cache-ttl) | "120" | **`INI_SYSTEM`** |  |

> **Зауваження** :
> 
> Использование[open\_basedir](ini.core.md#ini.open-basedir) *відключить*кеш realpath.

Коротке пояснення конфігураційних директив.

`realpath_cache_size`int

Визначає розмір кеша realpath, що використовується в PHP. Це значення має бути збільшено на системах, в яких PHP відкриває велику кількість файлів відповідно до кількості виконуваних файлових операцій.

Розмір дорівнює загальному числу байт, що зберігається в рядках шляхів, плюс розмір даних пов'язаних з елементом, що кешується. Це означає, що для зберігання довгих шляхів у кеші, розмір цього кешу має бути більшим. Це значення не визначає безпосередньо кількість різних шляхів, які можуть бути закешовані.

Розмір, необхідний кешування, залежить від системи.

`realpath_cache_ttl`int

Час (в секундах) протягом якого буде використаний кеш realpath для вказаного файлу або директорії. Для систем з файлами, що рідко змінюються, це значення можна збільшити.

## Обробка даних

**Конфігураційні опції обробки даних**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [arg\_separator.output](ini.core.md#ini.arg-separator.output) | "&" | **`INI_ALL`** |  |
| [arg\_separator.input](ini.core.md#ini.arg-separator.input) | "&" | **`INI_PERDIR`** |  |
| [variables\_order](ini.core.md#ini.variables-order) | "EGPCS" | **`INI_PERDIR`** |  |
| [request\_order](ini.core.md#ini.request-order) | "" | **`INI_PERDIR`** |  |
| [auto\_globals\_jit](ini.core.md#ini.auto-globals-jit) | "1" | **`INI_PERDIR`** |  |
| [register\_argc\_argv](ini.core.md#ini.register-argc-argv) | "1" | **`INI_PERDIR`** |  |
| [enable\_post\_data\_reading](ini.core.md#ini.enable-post-data-reading) | "1" | **`INI_PERDIR`** |  |
| [post\_max\_size](ini.core.md#ini.post-max-size) | "8M" | **`INI_PERDIR`** |  |
| [auto\_prepend\_file](ini.core.md#ini.auto-prepend-file) | NULL | **`INI_PERDIR`** |  |
| [auto\_append\_file](ini.core.md#ini.auto-append-file) | NULL | **`INI_PERDIR`** |  |
| [default\_mimetype](ini.core.md#ini.default-mimetype) | "text/html" | **`INI_ALL`** |  |
| [default\_charset](ini.core.md#ini.default-charset) | "UTF-8" | **`INI_ALL`** |  |
| [input\_encoding](ini.core.md#ini.input-encoding) | "" | **`INI_ALL`** |  |
| [output\_encoding](ini.core.md#ini.output-encoding) | "" | **`INI_ALL`** |  |
| [internal\_encoding](ini.core.md#ini.internal-encoding) | "" | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`arg_separator.output`string

Цей роздільник використовується в генерованих PHP URL як роздільник аргументів.

`arg_separator.input`string

Список роздільників, що використовуються PHP для отримання змінних із URL.

> **Зауваження** :
> 
> Кожен символ у цій директиві вважається роздільником!

`variables_order`string

Встановлює порядок обробки змінних EGPCS (`E`nvironment,`G`et,`P`ost,`C`ookie, и`S`server). Наприклад, якщо variables\_order установлена в`"SP"`, то PHP створить [superglobals](language.variables.predefined.md) [$\_SERVER](reserved.variables.server.md) і [$\_POST](reserved.variables.post.md), але не буде створювати [$\_ENV](reserved.variables.environment.md) [$\_GET](reserved.variables.get.md) і [$\_COOKIE](reserved.variables.cookies.md). . Установка в "" означає, що жодна [superglobals](language.variables.predefined.md)не будет установлена.

**Увага**

У CGI та FastCGI SAPI, [$\_SERVER](reserved.variables.server.md) також додаються значення змінних оточення; `S` завжди еквівалентна `ES`вне зависимости от самого положения`E` у цій директиві.

> **Зауваження** :
> 
> Ця директива також впливає на вміст та порядок змінної [$\_REQUEST](reserved.variables.request.md)

`request_order`string

Ця директива регулює порядок, в якому PHP додає змінні GET, POST та Cookie до масиву. \_REQUEST. Додавання проводиться ліворуч, нові значення перезаписують старі.

Якщо значення цієї директиви не встановлено, використовується значення директиви [variables\_order](ini.core.md#ini.variables-order)для содержимого переменной[$\_REQUEST](reserved.variables.request.md)

Зверніть увагу, що файли php.ini, що поставляються з дистрибутивом, з міркувань безпеки не містять значення `'C'`(cookies).

`auto_globals_jit`bool

Коли увімкнено, змінні SERVER, REQUEST та ENV створюються в той момент, коли вони вперше використовуються (Just In Time), а не на початку виконання скрипту. Якщо ці змінні у скрипті не використовуються, включення цієї директиви призведе до зростання продуктивності.

**Увага**

Використання змінних SERVER, REQUEST та ENV перевіряється на стадії компіляції, тому їх використання за допомогою, наприклад, [змінних змінних](language.variables.variable.md)не запустит их инициализацию.

`register_argc_argv`bool

Повідомляє PHP, чи слід оголошувати змінні argv та argc (які міститимуть GET-інформацію). Дивіться також [Використання PHP у командному рядку](features.commandline.md)

`enable_post_data_reading`bool

При відключенні цієї опції суперглобальні змінні [$\_POST](reserved.variables.post.md) і [$\_FILES](reserved.variables.files.md) *не будуть* заповнюватись. Єдиним способом прочитати POST-дані буде читання обгортки потоку [php://input](wrappers.php.md). Це може бути корисним при проксуванні запитів або обробки POST-даних способом, що більш ефективно використовує пам'ять.

`post_max_size`int

Встановлює максимально допустимий розмір даних, які надсилаються методом POST. Це також впливає на завантаження файлів. Для завантаження великих файлів це значення має бути більшим за значення директиви [upload\_max\_filesize](ini.core.md#ini.upload-max-filesize). В сутності, [memory\_limit](ini.core.md#ini.memory-limit) має бути більше ніж `post_max_size`. Якщо вказано ціле значення (int), обсяг вимірюється байтами. Можна також використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes). Якщо розмір POST даних більше ніж post\_max\_size,[суперглобальні змінні](language.variables.superglobals.md) [$\_POST](reserved.variables.post.md) і [$\_FILES](reserved.variables.files.md) будуть порожніми. Це можна відстежити у різний спосіб, наприклад передавши [$\_GET](reserved.variables.get.md) змінну скрипт, який обробляє дані, тобто . `<form action="edit.php?processed=1">`, а затем проверить, установлена ли переменная[$\_GET\['processed'\]](reserved.variables.get.md)

> **Зауваження** :
> 
> PHP дозволяє скорочення значень байтів, включаючи K (кіло), M (мега) та G (гіга). PHP автоматично перетворює всі ці скорочення. Будьте обережні з перевищенням діапазону 32-бітових цілих значень (якщо ви використовуєте 32-бітну версію), оскільки це призведе до помилки вашого скрипту.

**Список изменений`post_max_size`**

| Версия | Опис |
| --- | --- |
| 5.3.4 | Встановлення `post_max_size` = 0 не знімає обмеження, якщо контент має тип application/x-www-form-urlencoded або не зареєстрований у PHP. |
| 5.3.2 , 5.2.12 | Стало можливим зняти обмеження на розмір пост-запиту установкою `post_max_size` 0. |

`auto_prepend_file`string

Визначає ім'я файлу, який автоматично оброблятиметься перед основним файлом. Файл викликається так, ніби він був підключений за допомогою функції [require](function.require.md), так що [include\_path](ini.core.md#ini.include-path)также используется.

Специальное значение`none` відключає цю директиву.

`auto_append_file`string

Визначає ім'я файлу, який автоматично оброблятиметься після основного файлу. Файл викликається так, ніби він був підключений за допомогою функції [require](function.require.md), так що [include\_path](ini.core.md#ini.include-path) також використовується.

Специальное значение`none` відключає цю директиву.

> **Зауваження**: Якщо скрипт завершує роботу за допомогою [exit()](function.exit.md), auto-append*НЕ* виконується.

`default_mimetype`string

За промовчанням PHP виводить назву кодування в заголовку Content-Type. Якщо не потрібно передавати кодування, просто залиште цю опцію порожньою.

"media type" за замовчуванням встановлено як "text/html".

`default_charset`string

"UTF-8" є значенням за промовчанням і використовується як кодування за промовчанням для функцій [htmlentities()](function.mdentities.md) [html\_entity\_decode()](function.md-entity-decode.md) і [htmlspecialchars()](function.mdspecialchars.md), якщо параметр `encoding`не указан. Значение`default_charset` також використовується для вказівки кодування за промовчанням для функцій [iconv](book.iconv.md)якщо конфігураційні опції [`iconv.input_encoding`](iconv.configuration.md#ini.iconv.input-encoding) [`iconv.output_encoding`](iconv.configuration.md#ini.iconv.output-encoding) і [`iconv.internal_encoding`](iconv.configuration.md#ini.iconv.internal-encoding) не встановлені, і для функцій [mbstring](book.mbstring.md), якщо не встановлено [`mbstring.http_input`](mbstring.configuration.md#ini.mbstring.http-input) [`mbstring.http_output`](mbstring.configuration.md#ini.mbstring.http-output) [`mbstring.internal_encoding`](mbstring.configuration.md#ini.mbstring.internal-encoding)

Усі версії PHP використовують це значення як кодування для стандартного заголовка Content-Type, що надсилається PHP, якщо цей заголовок не перевизначений викликом функції [header()](function.header.md)

Не рекомендуется устанавливать`default_charset`в пустое значение.

`input_encoding`string

Ця опція використовується для багатобайтних модулів, таких як mbstring та iconv. За промовчанням порожньо.

`output_encoding`string

Ця опція використовується для багатобайтних модулів, таких як mbstring та iconv. За промовчанням порожньо.

`internal_encoding`string

Ця опція використовується для багатобайтних модулів, таких як mbstring та iconv. За промовчанням порожньо. У цьому випадку використовується [default\_charset](ini.core.md#ini.default-charset)

## Шляхи та Директорії

**Конфігураційні Опції Шляхів та Директорій**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [include\_path](ini.core.md#ini.include-path) | ".;/path/to/php/pear" | **`INI_ALL`** |  |
| [open\_basedir](ini.core.md#ini.open-basedir) | NULL | **`INI_ALL`** |  |
| [doc\_root](ini.core.md#ini.doc-root) | NULL | **`INI_SYSTEM`** |  |
| [user\_dir](ini.core.md#ini.user-dir) | NULL | **`INI_SYSTEM`** |  |
| [user\_ini.cache\_ttl](ini.core.md#ini.user-ini.cache-ttl) | "300" | **`INI_SYSTEM`** |  |
| [user\_ini.filename](ini.core.md#ini.user-ini.filename) | ".user.ini" | **`INI_SYSTEM`** |  |
| [extension\_dir](ini.core.md#ini.extension-dir) | "/path/to/php" | **`INI_SYSTEM`** |  |
| [extension](ini.core.md#ini.extension) | NULL | Тільки php.ini |  |
| [zend\_extension](ini.core.md#ini.zend-extension) | NULL | Тільки php.ini |  |
| [cgi.check\_shebang\_line](ini.core.md#ini.cgi.check-shebang-line) | "1" | **`INI_SYSTEM`** |  |
| [cgi.discard\_path](ini.core.md#ini.cgi.discard-path) | "0" | **`INI_SYSTEM`** |  |
| [cgi.fix\_pathinfo](ini.core.md#ini.cgi.fix-pathinfo) | "1" | **`INI_SYSTEM`** |  |
| [cgi.force\_redirect](ini.core.md#ini.cgi.force-redirect) | "1" | **`INI_SYSTEM`** |  |
| [cgi.nph](ini.core.md#ini.cgi.nph) | "0" | **`INI_SYSTEM`** |  |
| [cgi.redirect\_status\_env](ini.core.md#ini.cgi.redirect-status-env) | NULL | **`INI_SYSTEM`** |  |
| [cgi.rfc2616\_headers](ini.core.md#ini.cgi.rfc2616-headers) | "0" | **`INI_ALL`** |  |
| [fastcgi.impersonate](ini.core.md#ini.fastcgi.impersonate) | "0" | **`INI_SYSTEM`** |  |
| [fastcgi.logging](ini.core.md#ini.fastcgi.logging) | "1" | **`INI_SYSTEM`** |  |

Коротке пояснення конфігураційних директив.

`include_path`string

Вказує список директорій, у яких функції [require](function.require.md) [include](function.include.md) [fopen()](function.fopen.md) [file()](function.file.md) [readfile()](function.readfile.md) і [file\_get\_contents()](function.file-get-contents.md) шукають файли Формат відповідає формату системної змінної оточення PATH: список директорій, розділених двокрапкою в Unix або крапкою з комою у Windows.

При пошуку файлів, що підключаються, PHP окремо розглядає кожне значення в include\_path. Він перевіряє перший шлях, якщо файл у ньому не знайдений, то він переходить до наступного, і так до тих пір, поки не знайде файл, що підключається, або поверне **`E_WARNING`** або **`E_ERROR`**. Ви можете змінити ваш include\_path під час виконання скрипту за допомогою функції [set\_include\_path()](function.set-include-path.md)

**Приклад #1 include\_path в Unix**

include\_path=".:/php/includes"

**Приклад #2 include\_path у Windows**

include\_path=".;c:\\php\\includes"

Использование в include\_path дозволяє задавати відносні шляхи для підключення файлів, оскільки точка означає поточну директорію. Однак, більш ефективно використовувати `include './file'`чим змушувати PHP щоразу перевіряти поточну директорію при підключенні кожного файлу.

> **Зауваження** :
> 
> Змінні оточення (`ENV`) також доступні в .ini файлах. Таким чином, можна посилатися на домашню директорію за допомогою директив `${LOGIN}`и`${USER}`
> 
> Змінні оточення можуть відрізнятися між різними серверними API, оскільки самі оточення відрізняються один від одного.

**Приклад #3 Налаштування include\_path за допомогою змінної оточення ${USER} в Unix**

include\_path = ".:${USER}/pear/php"

`open_basedir`string

Обмежує зазначеним деревом каталогів файли, які можуть бути доступні для PHP, включаючи файл.

Коли скрипт намагається отримати доступ до файлу, наприклад, за допомогою функції [fopen()](function.fopen.md) або [gzopen()](function.gzopen.md), перевіряється місцезнаходження файлу. Якщо файл знаходиться поза вказаним деревом каталогів, PHP відмовиться його відкривати. Всі символічні посилання будуть розкриті, так що за їх допомогою не вдасться обійти це обмеження. Якщо файл не існує, то символічне посилання не може бути прочитане і ім'я файлу (прочитане) буде розглядатися **open\_basedir**

Опция**open\_basedir** може поширюватися як на функції до роботи з файлової системою; наприклад, якщо `MySQL` налаштований використовувати драйвер `mysqlnd`, то`LOAD DATA INFILE`подпадает под опцию**open\_basedir**. Безліч функцій PHP також використовує `open_basedir`

Специальное значение позначає, що робоча директорія скрипта буде використана як базова директорія. Однак це трохи небезпечно, так як поточна директорія скрипту може бути легко змінена за допомогою [chdir()](function.chdir.md)

В httpd.conf,**open\_basedir** може бути вимкнена (наприклад, для деяких віртуальних хостів) [тим же способом](configuration.changes.md#configuration.changes.apache), як і будь-яка інша конфігураційна директива: "`php_admin_value open_basedir none`".

У Windows розділяйте каталоги крапкою з комою. На всіх інших системах, розділяйте директорії двокрапкою. При роботі в якості модуля Apache, шляхи **open\_basedir** автоматично успадковуються від батьківських директорій.

Ограничение, определяемое**open\_basedir** є ім'ям директорії, а чи не префіксом.

За промовчанням всі файли можуть бути відкриті.

> **Зауваження** :
> 
> Значення open\_Basedir можна зробити суворішим під час виконання скрипту. Це означає, що якщо open\_basedir була встановлена ​​в `/www/` в php.ini, то скрипт може утиснути конфігурацію до `/www/tmp/` під час виконання за допомогою [ini\_set()](function.ini-set.md). При вказівці кількох директорій можна використовувати константу **`PATH_SEPARATOR`** як роздільник шляхів, який залежить від операційної системи.

> **Зауваження** :
> 
> Використання опції open\_basedir установит[realpath\_cache\_size](ini.core.md#ini.realpath-cache-size)на значение и таким образом*відключить*кеш realpath.

**Застереження**

`open_basedir` - це просто додаткове підстрахування, яке аж ніяк не є всеосяжним і тому на нього не можна покладатися, коли йдеться про безпеку.

`doc_root`string

Коренева директорія PHP на цьому сервері. Використовується лише у випадку, якщо не пуста. Якщо PHP не був скомпільований з FORCE\_REDIRECT, вам*слід*установить doc\_root, якщо ви використовуєте PHP як CGI під будь-яким веб-сервером (крім IIS). Альтернативою є використання конфігураційної директиви [cgi.force\_redirect](ini.core.md#ini.cgi.force-redirect), Мова про яку йде нижче.

`user_ini.cache_ttl`int

`user_ini.filename`string

`user_dir`string

Базове ім'я директорії, що використовується в домашньому каталозі користувача для файлів PHP, наприклад, public\_html.

`extension_dir`string

У якій директорії PHP повинен шукати модулі, що динамічно завантажуються. Рекомендується вказувати абсолютний шлях. Дивіться також: [enable\_dl](info.configuration.md#ini.enable-dl) і [dl()](function.dl.md)

`extension`string

Які модулі, що динамічно завантажуються, повинні бути завантажені при старті PHP.

`zend_extension`string

Ім'я модуля Zend (наприклад, XDebug), що динамічно завантажується, який повинен бути завантажений при старті PHP.

`cgi.check_shebang_line`bool

Контролює, чи потрібно перевіряти перший рядок CGI PHP-скрипту на зміст `#!` (Shebang). Цей рядок може бути необхідним, якщо скрипт повинен підтримувати як окремий запуск, так і за допомогою PHP CGI. PHP у режимі CGI пропускає цей рядок і ігнорує його вміст, якщо ця директива включена.

`cgi.discard_path`bool

Якщо дозволено, бінарний файл PHP CGI може безпечно розташовуватися поза веб-деревом і люди не зможуть обійти безпеку .htaccess.

`cgi.fix_pathinfo`bool

Забезпечує підтримку *правильних* `PATH_INFO` `PATH_TRANSLATED`в CGI. Раньше PHP просто устанавливал`PATH_TRANSLATED`в`SCRIPT_FILENAME`и не обращал внимания на`PATH_INFO`. Для отримання додаткової інформації про `PATH_INFO`зверніться до специфікації CGI. Встановлення цього значення змусить PHP CGI виправляти свій шлях відповідно до специфікації. Значення 0 відповідає попередньому поведінці. За замовчуванням опція увімкнена. Ви повинні виправити свої скрипти так, щоб вони використовували `SCRIPT_FILENAME` замість `PATH_TRANSLATED`

`cgi.force_redirect`bool

Директива cgi.force\_redirect необхідна для забезпечення безпеки під час роботи PHP як CGI під більшістю веб-серверів. Якщо залишити її невизначеною, PHP включає цю директиву. Ви можете вимкнути її *на свій страх і ризик*

> **Зауваження** :
> 
> Користувачам Windows: У разі використання IIS ця опція *повинна* бути вимкнена. Те саме необхідно для OmniHTTPD і Xitami.

`cgi.nph`bool

Якщо cgi.nph дозволена, cgi примусово повертатиме код 200 на кожен запит.

`cgi.redirect_status_env`string

Якщо cgi.force\_redirect включено і ви працюєте не під веб-сервером Apache або Netscape (iPlanet), вам *може* знадобиться встановити змінну оточення, яку шукатиме PHP щоб переконатися, що він може продовжувати виконання.

> **Зауваження** :
> 
> Встановлення цієї змінної *може* спричинити проблеми з безпекою, так що *ви повинні знати, що ви робите*

`cgi.rfc2616_headers`int

Повідомляє PHP, який тип заголовків використовувати при надсиланні коду відповіді HTTP. Якщо встановлено 0, PHP відправляє [» RFC 3875](http://www.faqs.org/rfcs/rfc3875) заголовок "Status:", який підтримується Apache та іншими веб-серверами. Якщо встановлено в 1, PHP надсилає заголовки, відповідні [» RFC 2616](http://www.faqs.org/rfcs/rfc2616)

Якщо ця опція включена і ви використовуєте PHP в оточенні CGI (наприклад, PHP-FPM), замість використання HTTP-заголовків відповіді в стилі RFC 2616, потрібно використовувати їх еквівалент зі стандарту RFC 3875, наприклад, замість header("HTTP/1.0 404 Not found"); потрібно використовувати header("Status: 404 Not Found");

Залиште значення 0, якщо ви не впевнені в тому, що це означає.

`fastcgi.impersonate`string

FastCGI під IIS (в ОС на базі WINNT) підтримує можливість імперсонації прав безпеки клієнта, що викликає. Це дозволяє IIS визначити контекст безпеки, у якому виконується запит. mod\_fastcgi під Apache на даний момент не підтримує цю можливість (03/17/2002). Встановіть 1 під час роботи під IIS. Значення за замовчуванням – нуль.

`fastcgi.logging`bool

Включає логування SAPI під час використання FastCGI. Логування увімкнено за замовчуванням.

## Закачування файлів

**Конфігураційні Опції Закачування файлів**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [file\_uploads](ini.core.md#ini.file-uploads) | "1" | **`INI_SYSTEM`** |  |
| [upload\_tmp\_dir](ini.core.md#ini.upload-tmp-dir) | NULL | **`INI_SYSTEM`** |  |
| [max\_input\_nesting\_level](info.configuration.md#ini.max-input-nesting-level) | 64 | **`INI_PERDIR`** |  |
| [max\_input\_vars](info.configuration.md#ini.max-input-vars) | 1000 | **`INI_PERDIR`** |  |
| [upload\_max\_filesize](ini.core.md#ini.upload-max-filesize) | "2M" | **`INI_PERDIR`** |  |
| [max\_file\_uploads](ini.core.md#ini.max-file-uploads) | 20 | **`INI_PERDIR`** |  |

Коротке пояснення конфігураційних директив.

`file_uploads`bool

Дозволяти чи не дозволяти [закачування файлів](features.file-upload.md). Дивіться також директиви [upload\_max\_filesize](ini.core.md#ini.upload-max-filesize) [upload\_tmp\_dir](ini.core.md#ini.upload-tmp-dir) і [post\_max\_size](ini.core.md#ini.post-max-size)

`upload_tmp_dir`string

Тимчасова директорія, що використовується для зберігання файлів під час закачування. Має бути доступною для запису користувачеві, від імені якого запущено PHP. Якщо не вказано, використовується каталог за промовчанням для вашої системи.

Якщо до зазначеної директорії немає прав на запис, PHP відкотиться назад до системної тимчасової директорії, яка використовується за умовчанням. Якщо увімкнено директиву [open\_basedir](ini.core.md#ini.open-basedir), то для успішного завантаження файлів системна директорія за умовчанням має бути дозволена.

`upload_max_filesize`int

Максимальний розмір файлу, що закачується.

[post\_max\_size](ini.core.md#ini.post-max-size) має бути більше, ніж це значення.

Якщо вказано ціле значення (int), обсяг вимірюється байтами. Можна також використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes)

`max_file_uploads`int

Максимально дозволена кількість файлів, що одночасно закачуються. Порожні поля завантаження не розглядаються цим обмеженням.

## Загальний SQL

**Конфігураційні Опції Загального SQL**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [sql.safe\_mode](ini.core.md#ini.sql.safe-mode) | "0" | **`INI_SYSTEM`** | Видалено в PHP 7.2.0 |

Коротке пояснення конфігураційних директив.

`sql.safe_mode`bool

Якщо увімкнено, функції з'єднання з базою даних, що використовують значення за замовчуванням, будуть використовувати ці значення замість будь-яких аргументів, що передаються. Для значень за замовчуванням дивіться документацію щодо функцій підключення відповідної бази даних.

**Увага**

Ця опція *ВИДАЛЕНО* у PHP 7.2.0.

## Особливі налаштування для Windows

**Особливі опції конфігурації для Windows**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [windows.show\_crt\_warning](ini.core.md#ini.windows-show-crt-warning) | "0" | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`windows.show_crt_warning`bool

При ввімкненні цієї директиви буде відображено попередження Windows CRT.
