Налаштування під час виконання

-   [« Установка](errorfunc.installation.html)
    
-   [Типы ресурсов »](errorfunc.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](errorfunc.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Налаштування конфігурації протоколювання подій та помилок**

| Имя                                                                             | По умолчанию | Место изменения | Список изменений                                        |
|---------------------------------------------------------------------------------|--------------|-----------------|---------------------------------------------------------|
| [errorreporting](errorfunc.configuration.html#ini.error-reporting)              | NULL         | PHPINIALL       |                                                         |
| [displayerrors](errorfunc.configuration.html#ini.display-errors)                | "1"          | PHPINIALL       |                                                         |
| [displaystartuperrors](errorfunc.configuration.html#ini.display-startup-errors) | "1"          | PHPINIALL       | До PHP 8.0.0 значення за промовчанням було `"0"`        |
| [logerrors](errorfunc.configuration.html#ini.log-errors)                        | "0"          | PHPINIALL       |                                                         |
| [logerrorsmaxlen](errorfunc.configuration.html#ini.log-errors-max-len)          | "1024"       | PHPINIALL       |                                                         |
| [ignorerepeatederrors](errorfunc.configuration.html#ini.ignore-repeated-errors) | "0"          | PHPINIALL       |                                                         |
| [ignorerepeatedsource](errorfunc.configuration.html#ini.ignore-repeated-source) | "0"          | PHPINIALL       |                                                         |
| [reportmemleaks](errorfunc.configuration.html#ini.report-memleaks)              | "1"          | PHPINIALL       |                                                         |
| [trackerrors](errorfunc.configuration.html#ini.track-errors)                    | "0"          | PHPINIALL       | Оголошено застарілим у PHP 7.2.0, видалено у PHP 8.0.0. |
| [htmlerrors](errorfunc.configuration.html#ini.html-errors)                      | "1"          | PHPINIALL       |                                                         |
| [xmlrpcerrors](errorfunc.configuration.html#ini.xmlrpc-errors)                  | "0"          | PHPINISYSTEM    |                                                         |
| [xmlrpcerrornumber](errorfunc.configuration.html#ini.xmlrpc-error-number)       | "0"          | PHPINIALL       |                                                         |
| [docrefroot](errorfunc.configuration.html#ini.docref-root)                      | ""           | PHPINIALL       |                                                         |
| [docrefext](errorfunc.configuration.html#ini.docref-ext)                        | ""           | PHPINIALL       |                                                         |
| [errorprependstring](errorfunc.configuration.html#ini.error-prepend-string)     | NULL         | PHPINIALL       |                                                         |
| [errorappendstring](errorfunc.configuration.html#ini.error-append-string)       | NULL         | PHPINIALL       |                                                         |
| [errorlog](errorfunc.configuration.html#ini.error-log)                          | NULL         | PHPINIALL       |                                                         |
| [syslog.facility](errorfunc.configuration.html#ini.syslog.facility)             | "LOGUSER"    | PHPINISYSTEM    | Доступно з PHP 7.3.0.                                   |
| [syslog.filter](errorfunc.configuration.html#ini.syslog.filter)                 | "no-ctrl"    | PHPINIALL       | Доступно з PHP 7.3.0.                                   |
| [syslog.ident](errorfunc.configuration.html#ini.syslog.ident)                   | "php"        | PHPINISYSTEM    | Доступно з PHP 7.3.0.                                   |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`error_reporting` int

Визначає рівень протоколювання помилки. Параметр може бути чисельністю, що представляє бітове поле, чи іменованою константою. Відповідні рівні та константи наведені у розділі [Предопределённые константы](errorfunc.constants.html), а також у php.ini. Для встановлення налаштувань під час виконання використовуйте функцію [errorreporting()](function.error-reporting.html). Дивіться також опис директиви [displayerrors](errorfunc.configuration.html#ini.display-errors)

Значення за умовчанням дорівнює **`E_ALL`**

До PHP 8.0.0 значення за промовчанням було: `E_ALL`\*\* & ~**`E_NOTICE`** & ~**`E_STRICT`** & ~\*\*`E_DEPRECATED`\*\*\`\`\*\*. При цьому налаштуванні не відображаються рівні помилок **`E_NOTICE`** **`E_STRICT`** і **`E_DEPRECATED`**

> **Зауваження** **PHP-константи за межами PHP**
> 
> Використання PHP-констант за межами PHP, наприклад, у файлі httpd.conf, не має сенсу, оскільки в таких випадках потрібні цілочисельні значення (int). Більше того, з часом будуть додаватися нові рівні помилок, а максимальне значення константи **`E_ALL`** відповідно зростатиме. Тому в місці, де передбачається вказати \*\*`E_ALL`\*\*краще задати велике ціле число, щоб перекрити всі можливі бітові поля. Таким числом може бути, наприклад, `2147483647` (воно включить усі можливі помилки, не тільки **`E_ALL`**

`display_errors` string

Ця установка визначає, чи потрібно виводити помилки на екран разом з рештою висновку, чи помилки повинні бути приховані від користувача.

Значення `"stderr"` посилає помилки в потік `stderr` замість `stdout`

> **Зауваження**
> 
> Ця функціональність призначена тільки для розробки і не повинна використовуватись у готових виробничих системах (наприклад, системах, які мають доступ до Інтернету).

> **Зауваження**
> 
> Незважаючи на те, що displayerrors може бути встановлена ​​під час виконання (функцією [iniset()](function.ini-set.html)), це ні на що не вплине, якщо у скрипті є фатальні помилки. Це пов'язано з тим, що очікувані дії програми під час виконання не отримають управління (не виконуватимуться).

`display_startup_errors` bool

Навіть якщо displayerrors включена, помилки, що виникають під час запуску PHP, не відображатимуться. Наполегливо рекомендуємо включати директиву displaystartuperrors тільки для налагодження.

`log_errors` bool

Відповідає за вибір журналу, де зберігатимуться повідомлення про помилки. Це може бути журнал сервера або [errorlog](errorfunc.configuration.html#ini.error-log). Застосовність цього параметра залежить від конкретного сервера.

> **Зауваження**
> 
> Настійно рекомендуємо при роботі на готових веб-сайтах, що працюють, протоколювати помилки там, де вони відображаються.

`log_errors_max_len` int

Завдання максимальної довжини logerrors у байтах. У [errorlog](errorfunc.configuration.html#ini.error-log) додається інформація про джерело. Значення за умовчанням 1024. Встановлення значення 0 дозволяє зняти обмеження на довжину logerrors. Це обмеження поширюється на помилки, що записуються в журнал, на помилки, що відображаються, а також на [$phperrormsg](reserved.variables.phperrormsg.html), але не на явно викликані функції, такі як [errorlog()](function.error-log.html)

Якщо використовується int значення вимірюється байтами. Ви також можете використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.html#faq.using.shorthandbytes)

`ignore_repeated_errors` bool

Не заносити в журнал помилки, що повторюються. Помилка вважається повторюваною, якщо відбувається в тому ж файлі і в тому ж рядку, і якщо налаштування [ignorerepeatedsource](errorfunc.configuration.html#ini.ignore-repeated-source) вимкнено.

`ignore_repeated_source` bool

Ігнорувати джерело помилок при пропуску повідомлень, що повторюються. Коли ця настройка увімкнена, повідомлення про помилки, що повторюються, не будуть заноситись до журналу незалежно від того, в яких файлах і рядках вони відбуваються.

`report_memleaks` bool

Якщо налаштування увімкнено (за замовчуванням), буде формуватися звіт про витік пам'яті, зафіксований менеджером пам'яті Zend. На POSIX платформах цей звіт надсилатиметься в потік stderr. На Windows платформах він надсилатиметься в налагоджувач функцією OutputDebugString(), переглянути звіт у цьому випадку можна за допомогою утиліт, начебто [» DbgView](http://technet.microsoft.com/en-us/sysinternals/bb896647). Ця настройка має сенс у збираннях, призначених для налагодження. При цьому **`E_WARNING`** повинна бути включена до списку errorreporting.

`track_errors` bool

Якщо включена, остання помилка буде першою в змінній [$phperrormsg](reserved.variables.phperrormsg.html)

`html_errors` bool

Якщо дозволено, повідомлення про помилки включатимуть теги HTML. Формат для HTML-помилок робить посилання, що натискаються, що ведуть на опис помилки, або функції, в якій вона відбулася. За такі посилання відповідальні [docrefroot](errorfunc.configuration.html#ini.docref-root) і [docrefext](errorfunc.configuration.html#ini.docref-ext)

Якщо заборонено, то помилки видаватимуться простим текстом, без форматування.

`xmlrpc_errors` bool

Якщо увімкнено, то нормальне сповіщення про помилки відключається і замість нього помилки виводяться у форматі XML-RPC.

`xmlrpc_error_number` int

Використовується як значення XML-RPC елемента faultCode.

`docref_root` string

Новий формат помилок містить посилання на сторінку з описом помилки або функції, що спричинила цю помилку. Можна розмістити копію описів помилок і функцій локально і задати ini директиві значення URL цієї копії. Якщо, наприклад, локальна копія описів доступна за адресою `"/manual/"`достатньо прописати **`docref_root=/manual/`**. Додатково необхідно задати значення директиві docrefext, що відповідає за відповідність розширень файлів файлам описів вашої локальної копії, **`docref_ext=.html`**. Також можливе використання зовнішніх посилань. Наприклад, **`docref_root=http://manual/en/`** або **`docref_root="http://landonize.it/?how=url&theme=classic&filter=Landon &url=http%3A%2F%2Fwww.php.net%2F"`**

У більшості випадків вам знадобиться значення docrefroot закінчувалося слішем `"/"`. Тим не менш, трапляються випадки, коли це не потрібно (дивіться вище, другий приклад).

> **Зауваження**
> 
> Ця функціональність призначена лише розробки, оскільки він полегшує пошук описів функцій і помилок. Не використовуйте його у готових виробничих системах (наприклад, які мають доступ до Інтернету).

`docref_ext` string

Дивіться [docrefroot](errorfunc.configuration.html#ini.docref-root)

> **Зауваження**
> 
> Значення docrefext має починатися з точки `"."`

`error_prepend_string` string

Рядок, який буде виводитися безпосередньо перед повідомленням про помилку. Використовується лише тоді, коли на екрані з'являється повідомлення про помилку. Основна мета – додати додаткову HTML-розмітку до повідомлення про помилку.

`error_append_string` string

Рядок, який виводиться після повідомлення про помилку. Використовується лише тоді, коли на екрані з'являється повідомлення про помилку. Основна мета – додати додаткову HTML-розмітку до повідомлення про помилку.

`error_log` string

Ім'я файлу, до якого будуть додаватися повідомлення про помилки. Файл повинен бути відкритим для запису користувача веб-сервера. Якщо використовується спеціальне значення `syslog`, то повідомлення будуть надсилатися до системного журналу. На Unix-системах це syslog(3), Windows NT - журнал подій. Дивіться також: [syslog()](function.syslog.html). Якщо директива не вказана, помилки будуть надсилатися до журналів SAPI. Наприклад, це можуть бути журнали помилок Apache або потік `stderr` командний рядок CLI. Також дивіться функцію [errorlog()](function.error-log.html)

`syslog.facility` string

Вказує, який тип програми реєструє повідомлення. Діє лише у тому випадку, якщо опція [errorlog](errorfunc.configuration.html#ini.error-log) встановлена ​​в "syslog".

`syslog.filter` string

Вказує тип фільтра для фільтрації повідомлень, що реєструються. Дозволені символи передаються без змін; всі інші записуються в шістнадцятковому поданні з префіксом `\x`

-   `all` – рядок буде поділено на символи нового рядка і всі символи будуть передані без змін
-   `ascii` – рядок буде поділено на символи нового рядка, а будь-які недруковані 7-бітові символи ASCII будуть екрановані
-   `no-ctrl` – рядок буде розділено на символи нового рядка, а будь-які символи, що не друкуються, будуть екрановані
-   `raw` – всі символи передаються до системного журналу без змін, без поділу на нові рядки (ідентично PHP до 7.3)

Параметр впливає на ведення журналу через [errorlog](errorfunc.configuration.html#ini.error-log) встановленого в "syslog" та виклики [syslog()](function.syslog.html)

> **Зауваження**
> 
> Тип фільтра `raw` доступний починаючи з PHP 7.3.8 та PHP 7.4.0.

Директива не підтримується у Windows.

`syslog.ident` string

Визначає рядок ідентифікатора, який додається до кожного повідомлення. Діє лише у тому випадку, якщо опція [errorlog](errorfunc.configuration.html#ini.error-log) встановлена ​​в "syslog".