Налаштування під час виконання

-   [« Установка](info.installation.html)
    
-   [Типы ресурсов »](info.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](info.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Установки PHP/Параметри конфігурації інформації**

| Имя                                                                               | По умолчанию | Место изменения | Список изменений                                                        |
|-----------------------------------------------------------------------------------|--------------|-----------------|-------------------------------------------------------------------------|
| [assert.active](info.configuration.html#ini.assert.active)                        | "1"          | PHPINIALL       |                                                                         |
| [assert.bail](info.configuration.html#ini.assert.bail)                            | "0"          | PHPINIALL       |                                                                         |
| [assert.warning](info.configuration.html#ini.assert.warning)                      | "1"          | PHPINIALL       |                                                                         |
| [assert.callback](info.configuration.html#ini.assert.callback)                    | NULL         | PHPINIALL       |                                                                         |
| [assert.quiet\_eval](info.configuration.html#ini.assert.quiet-eval)               | "0"          | PHPINIALL       |                                                                         |
| [assert.exception](info.configuration.html#ini.assert.exception)                  | "0"          | PHPINIALL       | Доступна з версії PHP 7.0.0.                                            |
| [enable\_dl](info.configuration.html#ini.enable-dl)                               | "1"          | PHPINISYSTEM    | Ця можливість застаріла та *буде* обов'язково *видалено* в майбутньому. |
| [max\_execution\_time](info.configuration.html#ini.max-execution-time)            | "30"         | PHPINIALL       |                                                                         |
| [max\_input\_time](info.configuration.html#ini.max-input-time)                    | "-1"         | PHPINIPERDIR    |                                                                         |
| [max\_input\_nesting\_level](info.configuration.html#ini.max-input-nesting-level) | "64"         | PHPINIPERDIR    | Доступна з PHP 5.2.3.                                                   |
| [max\_input\_vars](info.configuration.html#ini.max-input-vars)                    |              | PHPINIPERDIR    | Доступна з PHP 5.3.9.                                                   |
| [magic\_quotes\_gpc](info.configuration.html#ini.magic-quotes-gpc)                | "1"          | PHPINIPERDIR    | Видалено в PHP 5.4.0.                                                   |
| [magic\_quotes\_runtime](info.configuration.html#ini.magic-quotes-runtime)        | "0"          | PHPINIALL       | Видалено в PHP 5.4.0.                                                   |
| [zend.enable\_gc](info.configuration.html#ini.zend.enable-gc)                     | "1"          | PHPINIALL       | Доступна з PHP 5.3.0.                                                   |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`assert.active` bool

Увімкнення виконання [assert()](function.assert.html)

`assert.bail` bool

Завершення роботи скрипта під час провалу перевірки тверджень.

`assert.warning` bool

Виклик попереджень PHP для кожної проваленої перевірки затвердження.

`assert.callback` string

функція користувача, що викликається при провалі перевірки тверджень.

`assert.quiet_eval` bool

Використовуйте це налаштування функції [error\_reporting()](function.error-reporting.html) під час виконання перевірки тверджень. При увімкненні налаштування повідомлення про помилки під час перевірки тверджень не відображатимуться (неявний виклик errorreporting(0)). Якщо вимкнено налаштування, помилки будуть видаватися відповідно до налаштувань [error\_reporting()](function.error-reporting.html)

`assert.exception` bool

Генерує виняток [AssertionError](class.assertionerror.html) для невдалої перевірки затвердження.

`enable_dl` bool

Директива дозволяє вмикати та вимикати динамічне підвантаження модулів PHP за допомогою функції [dl()](function.dl.html)

Головною причиною, через яку потрібно вимкнення динамічного завантаження, є безпека. За допомогою динамічного завантаження можна обійти все [open\_basedir](ini.core.html#ini.open-basedir) обмеження. За замовчуванням динамічне завантаження дозволено.

`max_execution_time` int

Ця директива визначає максимальний час у секундах, протягом якого скрипт повинен повністю завантажитися. Якщо цього немає, парсер завершує роботу скрипта. Цей механізм допомагає запобігти зависанню сервера через погано написаний скрипт. За промовчанням на завантаження дається `30` секунд. Якщо PHP запущено з [командной строки](features.commandline.html), це значення за умовчанням дорівнює `0`

У системах, відмінних від Windows, на максимальний час виконання не впливають системні дзвінки, потокові операції тощо. За додатковою інформацією звертайтесь до документації до функції [set\_time\_limit()](function.set-time-limit.html)

Веб-сервери зазвичай мають свої налаштування часу очікування, після перевищення якого самі завершують виконання скрипта PHP. В Apache є директива `Timeout`У IIS є функція CGI timeout. В обох випадках за промовчанням встановлено 300 секунд. Точне значення можна дізнатися з документації до веб-сервера.

`max_input_time` int

Ця директива визначає максимальний час у секундах, протягом якого скрипт повинен розібрати всі вхідні дані, передані запитами на кшталт POST або GET. Цей час вимірюється з моменту, коли PHP викликаний на сервері до моменту, коли скрипт починає виконуватися. Значення за замовчуванням `-1`що означає, що буде використовуватися [max\_execution\_time](info.configuration.html#ini.max-execution-time). Якщо встановити рівним `0`, то обмежень у часі не буде.

`max_input_nesting_level` int

Задає максимальну глибину вкладеності [входных переменных](language.variables.external.html) (тобто [$\_GET](reserved.variables.get.html) [$\_POST](reserved.variables.post.html)

`max_input_vars` int

Скільки [входных переменных](language.variables.external.html) може бути прийнято в одному запиті (обмеження накладається на кожну з глобальних змінних $GET, $POST та $COOKIE окремо). Використання цієї директиви знижує ймовірність збоїв у разі атак із використанням хеш-колізій. Якщо вхідних змінних більше, ніж встановлено директивою, викидається попередження **`E_WARNING`**а всі наступні змінні в запиті ігноруються.

`magic_quotes_gpc` bool

**Увага**

Ця можливість була оголошена *застарілої*, починаючи з PHP 5.3.0 і була *ВИДАЛЕНО* у PHP 5.4.0.

Встановлює режим magicquotes для GPC (Get/Post/Cookie) операцій. Якщо magicquotes включений, всі ' (одинарні лапки), " (подвійні лапки), (зворотний сліш) та NUL автоматично екрануються зворотним слешем.

Дивіться також [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.html)

`magic_quotes_runtime` bool

**Увага**

Ця можливість була оголошена *застарілої*, починаючи з PHP 5.3.0 і була *ВИДАЛЕНО* у PHP 5.4.0.

Якщо увімкнено директиву `magic_quotes_runtime`, більшість функцій, що повертають дані із зовнішніх джерел, таких як бази даних або текстові файли, будуть екранувати лапки зворотним слешем.

Функції, на які поширюється дія директиви `magic_quotes_runtime` (виключаючи функції з PECL):

-   [get\_meta\_tags()](function.get-meta-tags.html)
-   [file\_get\_contents()](function.file-get-contents.html)
-   [file()](function.file.html)
-   [fgets()](function.fgets.html)
-   [fwrite()](function.fwrite.html)
-   [fread()](function.fread.html)
-   [fputcsv()](function.fputcsv.html)
-   [stream\_socket\_recvfrom()](function.stream-socket-recvfrom.html)
-   [exec()](function.exec.html)
-   [system()](function.system.html)
-   [passthru()](function.passthru.html)
-   [stream\_get\_contents()](function.stream-get-contents.html)
-   [bzread()](function.bzread.html)
-   [gzfile()](function.gzfile.html)
-   [gzgets()](function.gzgets.html)
-   [gzwrite()](function.gzwrite.html)
-   [gzread()](function.gzread.html)
-   [exif\_read\_data()](function.exif-read-data.html)
-   [dba\_insert()](function.dba-insert.html)
-   [dba\_replace()](function.dba-replace.html)
-   [dba\_fetch()](function.dba-fetch.html)
-   [ibase\_fetch\_row()](function.ibase-fetch-row.html)
-   [ibase\_fetch\_assoc()](function.ibase-fetch-assoc.html)
-   [ibase\_fetch\_object()](function.ibase-fetch-object.html)
-   **mssqlfetchrow()**
-   **mssqlfetchobject()**
-   **mssqlfetcharray()**
-   **mssqlfetchassoc()**
-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.html)
-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.html)
-   [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.html)
-   [mysqli\_fetch\_object()](mysqli-result.fetch-object.html)
-   [pg\_fetch\_row()](function.pg-fetch-row.html)
-   [pg\_fetch\_assoc()](function.pg-fetch-assoc.html)
-   [pg\_fetch\_array()](function.pg-fetch-array.html)
-   [pg\_fetch\_object()](function.pg-fetch-object.html)
-   [pg\_fetch\_all()](function.pg-fetch-all.html)
-   [pg\_select()](function.pg-select.html)
-   **sybasefetchobject()**
-   **sybasefetcharray()**
-   **sybasefetchassoc()**
-   [SplFileObject::fgets()](splfileobject.fgets.html)
-   [SplFileObject::fgetcsv()](splfileobject.fgetcsv.html)
-   [SplFileObject::fwrite()](splfileobject.fwrite.html)

`zend.enable_gc` bool

Включає або вимикає збирач циклічних посилань.