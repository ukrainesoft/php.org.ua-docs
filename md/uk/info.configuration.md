---
navigation:
  - info.installation.md: « Установка
  - info.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - info.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Установки PHP/Параметри конфігурації інформації**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [assert.active](info.configuration.md#ini.assert.active) | "1" | PHPINIALL |  |
| [assert.bail](info.configuration.md#ini.assert.bail) | "0" | PHPINIALL |  |
| [assert.warning](info.configuration.md#ini.assert.warning) | "1" | PHPINIALL |  |
| [assert.callback](info.configuration.md#ini.assert.callback) | NULL | PHPINIALL |  |
| [assert.quieteval](info.configuration.md#ini.assert.quiet-eval) | "0" | PHPINIALL |  |
| [assert.exception](info.configuration.md#ini.assert.exception) | "0" | PHPINIALL | Доступна з версії PHP 7.0.0. |
| [enableдл](info.configuration.md#ini.enable-dl) | "1" | PHPINISYSTEM | Ця можливість застаріла та *буде* обов'язково *видалено* в майбутньому. |
| [maxexecutiontime](info.configuration.md#ini.max-execution-time) | "30" | PHPINIALL |  |
| [maxinputtime](info.configuration.md#ini.max-input-time) | "-1" | PHPINIPERDIR |  |
| [maxinputnestinglevel](info.configuration.md#ini.max-input-nesting-level) | "64" | PHPINIPERDIR | Доступна з PHP 5.2.3. |
| [maxinputvars](info.configuration.md#ini.max-input-vars) |  | PHPINIPERDIR | Доступна з PHP 5.3.9. |
| [magicquotesgpc](info.configuration.md#ini.magic-quotes-gpc) | "1" | PHPINIPERDIR | Видалено в PHP 5.4.0. |
| [magicquotesruntime](info.configuration.md#ini.magic-quotes-runtime) | "0" | PHPINIALL | Видалено в PHP 5.4.0. |
| [zend.enableгк](info.configuration.md#ini.zend.enable-gc) | "1" | PHPINIALL | Доступна з PHP 5.3.0. |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`assert.active` bool

Увімкнення виконання [assert()](function.assert.md)

`assert.bail` bool

Завершення роботи скрипта під час провалу перевірки тверджень.

`assert.warning` bool

Виклик попереджень PHP для кожної проваленої перевірки затвердження.

`assert.callback` string

функція користувача, що викликається при провалі перевірки тверджень.

`assert.quiet_eval` bool

Використовуйте це налаштування функції [errorreporting()](function.error-reporting.md) під час виконання перевірки тверджень. При увімкненні налаштування повідомлення про помилки під час перевірки тверджень не відображатимуться (неявний виклик errorreporting(0)). Якщо вимкнено налаштування, помилки будуть видаватися відповідно до налаштувань [errorreporting()](function.error-reporting.md)

`assert.exception` bool

Генерує виняток [AssertionError](class.assertionerror.md) для невдалої перевірки затвердження.

`enable_dl` bool

Директива дозволяє вмикати та вимикати динамічне підвантаження модулів PHP за допомогою функції [dl()](function.dl.md)

Головною причиною, через яку потрібно вимкнення динамічного завантаження, є безпека. За допомогою динамічного завантаження можна обійти все [openbasedir](ini.core.md#ini.open-basedir) обмеження. За замовчуванням динамічне завантаження дозволено.

`max_execution_time` int

Ця директива визначає максимальний час у секундах, протягом якого скрипт повинен повністю завантажитися. Якщо цього немає, парсер завершує роботу скрипта. Цей механізм допомагає запобігти зависанню сервера через погано написаний скрипт. За промовчанням на завантаження дається `30` секунд. Якщо PHP запущено з [командного рядка](features.commandline.md), це значення за умовчанням дорівнює `0`

У системах, відмінних від Windows, на максимальний час виконання не впливають системні дзвінки, потокові операції тощо. За додатковою інформацією звертайтесь до документації до функції [settimelimit()](function.set-time-limit.md)

Веб-сервери зазвичай мають свої налаштування часу очікування, після перевищення якого самі завершують виконання скрипта PHP. В Apache є директива `Timeout`У IIS є функція CGI timeout. В обох випадках за промовчанням встановлено 300 секунд. Точне значення можна дізнатися з документації до веб-сервера.

`max_input_time` int

Ця директива визначає максимальний час у секундах, протягом якого скрипт повинен розібрати всі вхідні дані, передані запитами на кшталт POST або GET. Цей час вимірюється з моменту, коли PHP викликаний на сервері до моменту, коли скрипт починає виконуватися. Значення за замовчуванням `-1`що означає, що буде використовуватися [maxexecutiontime](info.configuration.md#ini.max-execution-time). Якщо встановити рівним `0`, то обмежень у часі не буде.

`max_input_nesting_level` int

Задає максимальну глибину вкладеності [вхідних змінних](language.variables.external.md) (тобто [GET](reserved.variables.get.md) [POST](reserved.variables.post.md)

`max_input_vars` int

Скільки [вхідних змінних](language.variables.external.md) може бути прийнято в одному запиті (обмеження накладається на кожну з глобальних змінних $GET, $POST та $COOKIE окремо). Використання цієї директиви знижує ймовірність збоїв у разі атак із використанням хеш-колізій. Якщо вхідних змінних більше, ніж встановлено директивою, викидається попередження \*\*`E_WARNING`\*\*а всі наступні змінні в запиті ігноруються.

`magic_quotes_gpc` bool

**Увага**

Ця можливість була оголошена *застарілої*, починаючи з PHP 5.3.0 і була *ВИДАЛЕНО* у PHP 5.4.0.

Встановлює режим magicquotes для GPC (Get/Post/Cookie) операцій. Якщо magicquotes включений, всі ' (одинарні лапки), " (подвійні лапки), (зворотний сліш) та NUL автоматично екрануються зворотним слешем.

Дивіться також [getmagicquotesgpc()](function.get-magic-quotes-gpc.md)

`magic_quotes_runtime` bool

**Увага**

Ця можливість була оголошена *застарілої*, починаючи з PHP 5.3.0 і була *ВИДАЛЕНО* у PHP 5.4.0.

Якщо увімкнено директиву `magic_quotes_runtime`, більшість функцій, що повертають дані із зовнішніх джерел, таких як бази даних або текстові файли, будуть екранувати лапки зворотним слешем.

Функції, на які поширюється дія директиви `magic_quotes_runtime` (виключаючи функції з PECL):

-   [getmetatags()](function.get-meta-tags.md)
-   [filegetcontents()](function.file-get-contents.md)
-   [file()](function.file.md)
-   [fgets()](function.fgets.md)
-   [fwrite()](function.fwrite.md)
-   [fread()](function.fread.md)
-   [fputcsv()](function.fputcsv.md)
-   [streamsocketrecvfrom()](function.stream-socket-recvfrom.md)
-   [exec()](function.exec.md)
-   [system()](function.system.md)
-   [passthru()](function.passthru.md)
-   [streamgetcontents()](function.stream-get-contents.md)
-   [bzread()](function.bzread.md)
-   [gzfile()](function.gzfile.md)
-   [gzgets()](function.gzgets.md)
-   [gzwrite()](function.gzwrite.md)
-   [gzread()](function.gzread.md)
-   [exifreaddata()](function.exif-read-data.md)
-   [dbainsert()](function.dba-insert.md)
-   [dbareplace()](function.dba-replace.md)
-   [dbafetch()](function.dba-fetch.md)
-   [ibasefetchrow()](function.ibase-fetch-row.md)
-   [ibasefetchassoc()](function.ibase-fetch-assoc.md)
-   [ibasefetchobject()](function.ibase-fetch-object.md)
-   **mssqlfetchrow()**
-   **mssqlfetchobject()**
-   **mssqlfetcharray()**
-   **mssqlfetchassoc()**
-   [mysqlifetchrow()](mysqli-result.fetch-row.md)
-   [mysqlifetcharray()](mysqli-result.fetch-array.md)
-   [mysqlifetchassoc()](mysqli-result.fetch-assoc.md)
-   [mysqlifetchobject()](mysqli-result.fetch-object.md)
-   [пгfetchrow()](function.pg-fetch-row.md)
-   [пгfetchassoc()](function.pg-fetch-assoc.md)
-   [пгfetcharray()](function.pg-fetch-array.md)
-   [пгfetchobject()](function.pg-fetch-object.md)
-   [пгfetchall()](function.pg-fetch-all.md)
-   [пгselect()](function.pg-select.md)
-   **sybasefetchobject()**
-   **sybasefetcharray()**
-   **sybasefetchassoc()**
-   [SplFileObject::fgets()](splfileobject.fgets.md)
-   [SplFileObject::fgetcsv()](splfileobject.fgetcsv.md)
-   [SplFileObject::fwrite()](splfileobject.fwrite.md)

`zend.enable_gc` bool

Включає або вимикає збирач циклічних посилань.
