---
navigation:
  - errorfunc.installation.md: « Встановлення
  - errorfunc.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - errorfunc.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Налаштування конфігурації протоколювання подій та помилок**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [error\_reporting](errorfunc.configuration.md#ini.error-reporting) | NULL | **`INI_ALL`** |  |
| [display\_errors](errorfunc.configuration.md#ini.display-errors) | "1" | **`INI_ALL`** |  |
| [display\_startup\_errors](errorfunc.configuration.md#ini.display-startup-errors) | "1" | **`INI_ALL`** | До PHP 8.0.0 значення за промовчанням було `"0"` |
| [log\_errors](errorfunc.configuration.md#ini.log-errors) | "0" | **`INI_ALL`** |  |
| [log\_errors\_max\_len](errorfunc.configuration.md#ini.log-errors-max-len) | "1024" | **`INI_ALL`** | Немає сенсу у версії PHP 8.0.0, видалено у версії PHP 8.1.0. |
| [ignore\_repeated\_errors](errorfunc.configuration.md#ini.ignore-repeated-errors) | "0" | **`INI_ALL`** |  |
| [ignore\_repeated\_source](errorfunc.configuration.md#ini.ignore-repeated-source) | "0" | **`INI_ALL`** |  |
| [report\_memleaks](errorfunc.configuration.md#ini.report-memleaks) | "1" | **`INI_ALL`** |  |
| [track\_errors](errorfunc.configuration.md#ini.track-errors) | "0" | **`INI_ALL`** | Оголошено застарілим у PHP 7.2.0, видалено у PHP 8.0.0. |
| [html\_errors](errorfunc.configuration.md#ini.md-errors) | "1" | **`INI_ALL`** |  |
| [xmlrpc\_errors](errorfunc.configuration.md#ini.xmlrpc-errors) | "0" | **`INI_SYSTEM`** |  |
| [xmlrpc\_error\_number](errorfunc.configuration.md#ini.xmlrpc-error-number) | "0" | **`INI_ALL`** |  |
| [docref\_root](errorfunc.configuration.md#ini.docref-root) | "" | **`INI_ALL`** |  |
| [docref\_ext](errorfunc.configuration.md#ini.docref-ext) | "" | **`INI_ALL`** |  |
| [error\_prepend\_string](errorfunc.configuration.md#ini.error-prepend-string) | NULL | **`INI_ALL`** |  |
| [error\_append\_string](errorfunc.configuration.md#ini.error-append-string) | NULL | **`INI_ALL`** |  |
| [error\_log](errorfunc.configuration.md#ini.error-log) | NULL | **`INI_ALL`** |  |
| [error\_log\_mode](errorfunc.configuration.md#ini.error-log-mode) | 0o644 | **`INI_ALL`** | Доступно, починаючи з PHP 8.2.0 |
| [syslog.facility](errorfunc.configuration.md#ini.syslog.facility) | "LOG\_USER" | **`INI_SYSTEM`** | Доступно з PHP 7.3.0. |
| [syslog.filter](errorfunc.configuration.md#ini.syslog.filter) | "no-ctrl" | **`INI_ALL`** | Доступно з PHP 7.3.0. |
| [syslog.ident](errorfunc.configuration.md#ini.syslog.ident) | "php" | **`INI_SYSTEM`** | Доступно з PHP 7.3.0. |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`error_reporting`int

Визначає рівень протоколювання помилки. Параметр може бути чисельністю, що представляє бітове поле, чи іменованою константою. Відповідні рівні та константи наведено у розділі [Обумовлені константи](errorfunc.constants.md) , а також у php.ini. Для встановлення налаштувань під час виконання використовуйте функцію [error\_reporting()](function.error-reporting.md). Дивіться також опис директиви [display\_errors](errorfunc.configuration.md#ini.display-errors)

Значение по умолчанию равно\*\*`E_ALL`\*\*

До PHP 8.0.0 значення за промовчанням було: **\`\`**`E_ALL`\*\* & ~**`E_NOTICE`** & ~**`E_STRICT`** & ~\*\*`E_DEPRECATED`\*\*\`\`\*\*. При цьому налаштуванні не відображаються рівні помилок **`E_NOTICE`** **`E_STRICT`**и**`E_DEPRECATED`**

> **Зауваження** **PHP-константи за межами PHP**
> 
> Використання PHP-констант за межами PHP, наприклад, у файлі httpd.conf, не має сенсу, оскільки в таких випадках потрібні цілочисельні значення (int). Більше того, з часом будуть додаватися нові рівні помилок, а максимальне значення константи **`E_ALL`** відповідно зростатиме. Тому в місці, де передбачається вказати \*\*`E_ALL`\*\*краще задати велике ціле число, щоб перекрити всі можливі бітові поля. Таким числом може бути, наприклад, `2147483647` (воно включить усі можливі помилки, не тільки **`E_ALL`**

`display_errors`string

Ця установка визначає, чи потрібно виводити помилки на екран разом з іншим виводом, чи помилки повинні бути приховані від користувача.

Значение`"stderr"` посилає помилки в потік `stderr` замість `stdout`

> **Зауваження** :
> 
> Ця функціональність призначена тільки для розробки і не повинна використовуватись у готових виробничих системах (наприклад, системах, які мають доступ до Інтернету).

> **Зауваження** :
> 
> Незважаючи на те, що display\_errors може бути встановлена ​​під час виконання (функцією [ini\_set()](function.ini-set.md)), це ні на що не вплине, якщо у скрипті є фатальні помилки. Це пов'язано з тим, що очікувані дії програми під час виконання не отримають управління (не виконуватимуться).

`display_startup_errors`bool

Навіть якщо display\_errors включена, помилки, що виникають під час запуску PHP, не відображатимуться. Наполегливо рекомендуємо включати директиву display\_startup\_errors тільки для налагодження.

`log_errors`bool

Відповідає за вибір журналу, де зберігатимуться повідомлення про помилки. Це може бути журнал сервера або [error\_log](errorfunc.configuration.md#ini.error-log). Застосовність цього параметра залежить від конкретного сервера.

> **Зауваження** :
> 
> Рекомендуємо при роботі на готових працюючих web сайтах протоколювати помилки там, де вони відображаються.

`log_errors_max_len`int

Завдання максимальної довжини log\_errors в байтах. В[error\_log](errorfunc.configuration.md#ini.error-log)добавляется информация об источнике. Значение по умолчанию 1024. Установка значения в 0 позволяет снять ограничение на длину log\_errors. Це обмеження поширюється на помилки, що записуються в журнал, на помилки, що відображаються, а також на [$php\_errormsg](reserved.variables.phperrormsg.md), але не на явно викликані функції, такі як [error\_log()](function.error-log.md)

Якщо вказано ціле значення (int), обсяг вимірюється байтами. Можна також використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes)

`ignore_repeated_errors`bool

Не заносити в журнал помилки, що повторюються. Помилка вважається повторюваною, якщо відбувається в тому ж файлі і в тому ж рядку, і якщо налаштування [ignore\_repeated\_source](errorfunc.configuration.md#ini.ignore-repeated-source) вимкнено.

`ignore_repeated_source`bool

Ігнорувати джерело помилок при пропуску повідомлень, що повторюються. Коли ця настройка увімкнена, повідомлення про помилки, що повторюються, не будуть заноситися до журналу незалежно від того, в яких файлах і рядках вони відбуваються.

`report_memleaks`bool

Якщо налаштування увімкнено (за замовчуванням), буде формуватися звіт про витік пам'яті, зафіксований менеджером пам'яті Zend. На POSIX платформах цей звіт надсилатиметься в потік stderr. На Windows платформах він надсилатиметься в налагоджувач функцією OutputDebugString(), переглянути звіт у цьому випадку можна за допомогою утиліт, начебто [» DbgView](http://technet.microsoft.com/en-us/sysinternals/bb896647). Ця настройка має сенс у збираннях, призначених для налагодження. При цьому **`E_WARNING`** повинна бути включена до списку error\_reporting.

`track_errors`bool

Якщо включена, остання помилка буде першою в змінній [$php\_errormsg](reserved.variables.phperrormsg.md)

`html_errors`bool

Якщо дозволено, повідомлення про помилки включатимуть теги HTML. Формат для HTML-помилок робить посилання, що натискаються, що ведуть на опис помилки, або функції, в якій вона відбулася. За такі посилання відповідальні [docref\_root](errorfunc.configuration.md#ini.docref-root) і [docref\_ext](errorfunc.configuration.md#ini.docref-ext)

Якщо заборонено, то помилки видаватимуться простим текстом, без форматування.

`xmlrpc_errors`bool

Якщо увімкнено, то нормальне сповіщення про помилки відключається і замість нього помилки виводяться у форматі XML-RPC.

`xmlrpc_error_number`int

Використовується як значення XML-RPC елемента faultCode.

`docref_root`string

Новий формат помилок містить посилання на сторінку з описом помилки або функції, що спричинила цю помилку. Можна розмістити копію описів помилок і функцій локально і задати ini директиві значення URL цієї копії. Якщо, наприклад, локальна копія описів доступна за адресою `"/manual/"`, достаточно прописать\*\*`docref_root=/manual/`\*\*Дополнительно, необходимо задать значение директиве docref\_ext, що відповідає за відповідність розширень файлів файлам описів вашої локальної копії, **`docref_ext=.md`**. Також можливе використання зовнішніх посилань. Наприклад, **`docref_root=http://manual/en/`**или**`docref_root="http://landonize.it/?how=url&theme=classic&filter=Landon &url=http%3A%2F%2Fwww.php.net%2F"`**

У більшості випадків вам знадобиться значення docref\_root закінчувалося слішем `"/"`. Тим не менш, трапляються випадки, коли це не потрібно (дивіться вище, другий приклад).

> **Зауваження** :
> 
> Ця функціональність призначена лише розробки, оскільки він полегшує пошук описів функцій і помилок. Не використовуйте його у готових виробничих системах (наприклад, які мають доступ до Інтернету).

`docref_ext`string

Смотрите[docref\_root](errorfunc.configuration.md#ini.docref-root)

> **Зауваження** :
> 
> Значення docref\_ext має починатися з точки `"."`

`error_prepend_string`string

Рядок, який буде виводитися безпосередньо перед повідомленням про помилку. Використовується лише тоді, коли на екрані з'являється повідомлення про помилку. Основна мета – додати додаткову HTML-розмітку до повідомлення про помилку.

`error_append_string`string

Рядок, який виводиться після повідомлення про помилку. Використовується лише тоді, коли на екрані з'являється повідомлення про помилку. Основна мета – додати додаткову HTML-розмітку до повідомлення про помилку.

`error_log`string

Ім'я файлу, до якого будуть додаватися повідомлення про помилки. Файл повинен бути відкритим для запису користувача веб-сервера. Якщо використовується спеціальне значення `syslog`, то повідомлення будуть надсилатися до системного журналу. На Unix-системах це syslog(3), Windows NT - журнал подій. Дивіться також: [syslog()](function.syslog.md). Якщо директива не задана, помилки будуть надсилатися до журналів SAPI. Наприклад, це можуть бути журнали помилок Apache або потік `stderr` командний рядок CLI. Також дивіться функцію [error\_log()](function.error-log.md)

`error_log_mode`int

Режим файла, описанного в[error\_log](errorfunc.configuration.md#ini.error-log)

`syslog.facility`string

Вказує, який тип програми реєструє повідомлення. Діє лише у тому випадку, якщо опція [error\_log](errorfunc.configuration.md#ini.error-log) встановлена ​​в "syslog".

`syslog.filter`string

Вказує тип фільтра для фільтрації повідомлень, що реєструються. Дозволені символи передаються без змін; всі інші записуються в шістнадцятковому поданні з префіксом `\x`

-   `all`– рядок буде поділено на символи нового рядка і всі символи будуть передані без змін
-   `ascii`– рядок буде поділено на символи нового рядка, а будь-які недруковані 7-бітові символи ASCII будуть екрановані
-   `no-ctrl`– рядок буде поділено на символи нового рядка, а будь-які символи, що не друкуються, будуть екрановані
-   `raw`– всі символи передаються до системного журналу без змін, без поділу на нові рядки (ідентично PHP до 7.3)

Параметр влияет на ведение журнала через[error\_log](errorfunc.configuration.md#ini.error-log) встановленого в "syslog" та виклики [syslog()](function.syslog.md)

> **Зауваження** :
> 
> Тип фильтра`raw` доступний починаючи з PHP 7.3.8 та PHP 7.4.0.

Директива не підтримується у Windows.

`syslog.ident`string

Визначає рядок ідентифікатора, який додається до кожного повідомлення. Діє лише у тому випадку, якщо опція [error\_log](errorfunc.configuration.md#ini.error-log) встановлена ​​в "syslog".
