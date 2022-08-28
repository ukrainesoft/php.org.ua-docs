Налаштування під час виконання

-   [« Установка](opcache.installation.html)
    
-   [Типы ресурсов »](opcache.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](opcache.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування OPcache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [opcache.enable](opcache.configuration.html#ini.opcache.enable) | "1" | PHPINIALL |  |
| [opcache.enable\_cli](opcache.configuration.html#ini.opcache.enable-cli) | "0" | PHPINISYSTEM | У версіях з PHP 7.1.2 до 7.1.6 включно, значення за замовчуванням "1" (включено) |
| [opcache.memory\_consumption](opcache.configuration.html#ini.opcache.memory-consumption) | "128" | PHPINISYSTEM |  |
| [opcache.interned\_strings\_buffer](opcache.configuration.html#ini.opcache.interned-strings-buffer) | "8" | PHPINISYSTEM |  |
| [opcache.max\_accelerated\_files](opcache.configuration.html#ini.opcache.max-accelerated-files) | "10000" | PHPINISYSTEM |  |
| [opcache.max\_wasted\_percentage](opcache.configuration.html#ini.opcache.max-wasted-percentage) | "5" | PHPINISYSTEM |  |
| [opcache.use\_cwd](opcache.configuration.html#ini.opcache.use-cwd) | "1" | PHPINISYSTEM |  |
| [opcache.validate\_timestamps](opcache.configuration.html#ini.opcache.validate-timestamps) | "1" | PHPINIALL |  |
| [opcache.revalidate\_freq](opcache.configuration.html#ini.opcache.revalidate-freq) | "2" | PHPINIALL |  |
| [opcache.revalidate\_path](opcache.configuration.html#ini.opcache.revalidate-path) | "0" | PHPINIALL |  |
| [opcache.save\_comments](opcache.configuration.html#ini.opcache.save-comments) | "1" | PHPINISYSTEM |  |
| [opcache.fast\_shutdown](opcache.configuration.html#ini.opcache.fast-shutdown) | "0" | PHPINISYSTEM |  |
| [opcache.enable\_file\_override](opcache.configuration.html#ini.opcache.enable-file-override) | "0" | PHPINISYSTEM |  |
| [opcache.optimization\_level](opcache.configuration.html#ini.opcache.optimization-level) | "0x7FFEBFFF" | PHPINISYSTEM | До PHP 7.3.0 було 0x7FFFBFFF |
| [opcache.inherited\_hack](opcache.configuration.html#ini.opcache.inherited-hack) | "1" | PHPINISYSTEM | Вилучено у PHP 7.3.0 |
| [opcache.dups\_fix](opcache.configuration.html#ini.opcache.dups-fix) | "0" | PHPINIALL |  |
| [opcache.blacklist\_filename](opcache.configuration.html#ini.opcache.blacklist-filename) | "" | PHPINISYSTEM |  |
| [opcache.max\_file\_size](opcache.configuration.html#ini.opcache.max-file-size) | "0" | PHPINISYSTEM |  |
| [opcache.consistency\_checks](opcache.configuration.html#ini.opcache.consistency-checks) | "0" | PHPINIALL |  |
| [opcache.force\_restart\_timeout](opcache.configuration.html#ini.opcache.force-restart-timeout) | "180" | PHPINISYSTEM |  |
| [opcache.error\_log](opcache.configuration.html#ini.opcache.error-log) | "" | PHPINISYSTEM |  |
| [opcache.log\_verbosity\_level](opcache.configuration.html#ini.opcache.log-verbosity-level) | "1" | PHPINISYSTEM |  |
| [opcache.record\_warnings](opcache.configuration.html#ini.opcache.record-warnings) | "0" | PHPINISYSTEM | Доступно з PHP 8.0.0. |
| [opcache.preferred\_memory\_model](opcache.configuration.html#ini.opcache.preferred-memory-model) | "" | PHPINISYSTEM |  |
| [opcache.protect\_memory](opcache.configuration.html#ini.opcache.protect-memory) | "0" | PHPINISYSTEM |  |
| [opcache.mmap\_base](opcache.configuration.html#ini.opcache.mmap-base) | **`null`** | PHPINISYSTEM |  |
| [opcache.restrict\_api](opcache.configuration.html#ini.opcache.restrict-api) | "" | PHPINISYSTEM |  |
| [opcache.file\_update\_protection](opcache.configuration.html#ini.opcache.file_update_protection) | "2" | PHPINIALL |  |
| [opcache.huge\_code\_pages](opcache.configuration.html#ini.opcache.huge_code_pages) | "0" | PHPINISYSTEM |  |
| [opcache.lockfile\_path](opcache.configuration.html#ini.opcache.lockfile_path) | "/tmp" | PHPINISYSTEM |  |
| [opcache.opt\_debug\_level](opcache.configuration.html#ini.opcache.opt_debug_level) | "0" | PHPINISYSTEM | Доступно з PHP 7.1.0 |
| [opcache.file\_cache](opcache.configuration.html#ini.opcache.file-cache) | NULL | PHPINISYSTEM |  |
| [opcache.file\_cache\_only](opcache.configuration.html#ini.opcache.file-cache-only) | "0" | PHPINISYSTEM |  |
| [opcache.file\_cache\_consistency\_checks](opcache.configuration.html#ini.opcache.file-cache-consistency-checks) | "1" | PHPINISYSTEM |  |
| [opcache.file\_cache\_fallback](opcache.configuration.html#ini.opcache.file-cache-fallback) | "1" | PHPINISYSTEM |  |
| [opcache.validate\_permission](opcache.configuration.html#ini.opcache.validate-permission) | "0" | PHPINISYSTEM | Доступно з PHP 7.0.14 |
| [opcache.validate\_root](opcache.configuration.html#ini.opcache.validate-root) | "0" | PHPINISYSTEM | Доступно з PHP 7.0.14 |
| [opcache.preload](opcache.configuration.html#ini.opcache.preload) | "" | PHPINISYSTEM | Доступно з PHP 7.4.0 |
| [opcache.preload\_user](opcache.configuration.html#ini.opcache.preload-user) | "" | PHPINISYSTEM | Доступно з PHP 7.4.0 |
| [opcache.cache\_id](opcache.configuration.html#ini.opcache.cache-id) | "" | PHPINISYSTEM | Тільки Windows. Доступно з PHP 7.4.0 |
| [opcache.jit](opcache.configuration.html#ini.opcache.jit) | "tracing" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_buffer\_size](opcache.configuration.html#ini.opcache.jit-buffer-size) | "0" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_debug](opcache.configuration.html#ini.opcache.jit-debug) | "0" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_bisect\_limit](opcache.configuration.html#ini.opcache.jit-bisect-limit) | "0" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_prof\_threshold](opcache.configuration.html#ini.opcache.jit-prof-threshold) | "0.005" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_root\_traces](opcache.configuration.html#ini.opcache.jit-max-root-traces) | "1024" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_side\_traces](opcache.configuration.html#ini.opcache.jit-max-side-traces) | "128" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_exit\_counters](opcache.configuration.html#ini.opcache.jit-max-exit-counters) | "8192" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_loop](opcache.configuration.html#ini.opcache.jit-hot-loop) | "64" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_func](opcache.configuration.html#ini.opcache.jit-hot-func) | "127" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_return](opcache.configuration.html#ini.opcache.jit-hot-return) | "8" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_side\_exit](opcache.configuration.html#ini.opcache.jit-hot-side-exit) | "8" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jit\_blacklist\_root\_trace](opcache.configuration.html#ini.opcache.jit-blacklist-root-trace) | "16" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_blacklist\_side\_trace](opcache.configuration.html#ini.opcache.jit-blacklist-side-trace) | "8" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_loop\_unrolls](opcache.configuration.html#ini.opcache.jit-max-loop-unrolls) | "8" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_recursive\_calls](opcache.configuration.html#ini.opcache.jit-max-recursive-calls) | "2" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_recursive\_returns](opcache.configuration.html#ini.opcache.jit-max-recursive-return) | "2" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_polymorphic\_calls](opcache.configuration.html#ini.opcache.jit-max-polymorphic-calls) | "2" | PHPINIALL | Доступно з PHP 8.0.0 |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`opcache.enable` bool

Дозволяє кешування опкодів. Якщо заборонено, код не оптимізуватиметься і не кешуватиметься. Опцію `opcache.enable` не можна увімкнути під час виконання за допомогою [ini\_set()](function.ini-set.html), але можна вимкнути. Спроба включити її у такий спосіб призведе до генерації попередження.

`opcache.enable_cli` bool

Дозволяє кешування опкодів для CLI-версії PHP.

`opcache.memory_consumption` int

Розмір пам'яті, що розділяється, в мегабайтах для OPcache. Мінімально допустиме значення - `"8"`, яке застосовується, якщо встановлено менше значення.

`opcache.interned_strings_buffer` int

Кількість пам'яті в мегабайтах для зберігання інтернованих рядків.

`opcache.max_accelerated_files` int

Максимальна кількість ключів (і, відповідно, скриптів) у хеш-таблиці OPcache. Фактичне значення буде першим числом з набору `{ 223, 463, 983, 1979, 3907, 7963, 16229, 32531, 65407, 130987, 262237, 524521, 1048793 }`, яке більше або дорівнює заданому в цьому параметрі. Мінімум 200, максимум 1000000. Значення за межами діапазону обмежені до допустимого діапазону.

`opcache.max_wasted_percentage` int

Максимальне значення втраченої пам'яті (у відсотках) після якого планується перезапуск, якщо недостатньо вільної пам'яті. Максимально допустиме значення: `"50"`, яка застосовується, якщо встановлено більше значення.

`opcache.use_cwd` bool

Якщо увімкнено, OPcache додає поточну робочу директорію до ключа скрипта, тим самим усуваючи можливість колізій для файлів з однаковим ім'ям. Вимкнення цієї опції підвищує продуктивність, але може призвести до збоїв.

`opcache.validate_timestamps` bool

Якщо увімкнено, OPcache перевірятиме актуальність закешованих скриптів кожні [opcache.revalidate\_freq](opcache.configuration.html#ini.opcache.revalidate-freq) секунд. Коли заборонено, ви можете перезапустити OPcache вручну за допомогою [opcache\_reset()](function.opcache-reset.html) [opcache\_invalidate()](function.opcache-invalidate.html) або перезапустити веб-сервер для того, щоб зміни набули чинності.

`opcache.revalidate_freq` int

Як часто в секундах перевіряти тимчасові мітки файлів . `0` призведе до того, що OPcache проводитиме цю перевірку при кожному запиті.

Ця директива ігнорується, якщо вимкнено [opcache.validate\_timestamps](opcache.configuration.html#ini.opcache.validate-timestamps)

`opcache.revalidate_path` bool

Якщо вимкнено, існуючі закешовані файли, які використовують один і той же [include\_path](ini.core.html#ini.include-path), повторно використовуватимуться. Таким чином, якщо файл з тим же ім'ям знаходиться в іншому місці в includepath, його не буде знайдено.

`opcache.save_comments` bool

Якщо вимкнено, всі коментарі будуть відкинуті з кешу опкодів для мінімізації розміру коду. Відключення цієї опції може призвести до того, що деякі фреймворки, що покладаються на анотації в коментарях, перестануть працювати, включаючи Doctrine, Zend Framework 2 та PHPUnit.

`opcache.fast_shutdown` bool

Якщо увімкнено, то буде використана швидка послідовність перезавантаження, при якій не відбувається очищення всіх виділених блоків пам'яті. Натомість для звільнення всього набору змінних використовується стандартний менеджер пам'яті Zend Engine.

Ця директива була видалена у PHP 7.2.0. Варіант швидкої послідовності перезавантаження був інтегрований у PHP і буде використовуватися, якщо це можливо.

`opcache.enable_file_override` bool

Якщо увімкнено, то кеш опкодів перевірятиме, чи вже закешовано файл при викликі функцій [file\_exists()](function.file-exists.html) [is\_file()](function.is-file.html) і [is\_readable()](function.is-readable.html). Це може підвищити продуктивність додатків, які перевіряють присутність і доступність для читання скриптом PHP, але несе ризик повернення застарілих даних, якщо заборонена опція [opcache.validate\_timestamps](opcache.configuration.html#ini.opcache.validate-timestamps)

`opcache.optimization_level` int

Бітова маска, яка контролює, які кроки оптимізації виконуються. За промовчанням застосовуються всі безпечні оптимізації. Зміна значення за промовчанням корисна для налагодження/розробки оптимізатора (див. також [opcache.opt\_debug\_level](opcache.configuration.html#ini.opcache.opt_debug_level)

`opcache.inherited_hack` bool

Ця директива ігнорується.

`opcache.dups_fix` bool

Цей хак потрібний лише для обходу помилок "Cannot redeclare class".

`opcache.blacklist_filename` string

Розташування чорного списку OPcache. Файл чорного списку містить імена файлів, які потрібно прискорювати, по одному запису на рядок. Допустимі шаблони пошуку та префікси. Рядки, що починаються з крапки з комою, ігноруються.

Приклад простого чорного списку:

```
; Указываем конкретный файл.
/var/www/broken.php
; Префикс, обозначающий все файлы, начинающиеся с x.
/var/www/x
; Шаблон поиска.
/var/www/*-broken.php
```

`opcache.max_file_size` int

Максимальний розмір файлу для кешування у байтах. Якщо поставити `0`, то кешуватимуться всі файли.

`opcache.consistency_checks` int

Якщо не нуль, OPcache звірятиме контрольну суму кешу кожні N запитів, де N - задане в цій директиві значення. Рекомендується включати лише при налагодженні, оскільки сильно впливає на продуктивність.

`opcache.force_restart_timeout` int

Кількість секунд очікування звільнення кеша, після якого буде примусово здійснено запланований перезапуск. Якщо цей час перевищено, OPcache вважає, що відбувається щось неправильне і вбиває процес блокування кешу.

Якщо параметр [opcache.log\_verbosity\_level](opcache.configuration.html#ini.opcache.log-verbosity-level) задати рівним 2 або більше, то, при виникненні такої ситуації, у лог помилок буде записано попередження.

Директива не підтримується у Windows.

`opcache.error_log` string

Лог помилок OPcache. Порожній рядок вважається як `stderr`і помилки будуть виведені в стандартний потік помилок (у більшості випадків це лог помилок веб-сервера).

`opcache.log_verbosity_level` int

Рівень подробиці помилок лога. За замовчуванням записуватимуться лише фатальні помилки (рівень 0) та помилки (рівень 1). Також значення можуть бути наступними: попередження (рівень 2), інформаційні повідомлення (рівень 3) та повідомлення налагодження (рівень 4).

`opcache.record_warnings` bool

Якщо увімкнено, OPcache запише попередження під час компіляції та відтворить їх при наступному увімкненні, навіть якщо воно виконується з кеша.

`opcache.preferred_memory_model` string

Вподобана модель пам'яті для OPcache. Якщо залишити порожнім, то OPcache самостійно вибере найбільш підходящу модель, яка поводитиметься коректно практично у будь-яких випадках.

Можливі значення включають `mmap` `shm` `posix` і `win32`

`opcache.protect_memory` bool

Захищає пам'ять від несподіваного запису під час запуску скриптів. Корисно тільки для внутрішнього налагодження.

`opcache.mmap_base` string

Базове значення для сегмента пам'яті, що розділяється в Windows. Всі процеси PHP повинні відображати пам'ять, що розділяється, в однаковий адресний простір. Ця опція допомагає полагодити помилки типу "Unable to reattach to base address".

`opcache.restrict_api` string

Дозволяє викликати функції API OPcache тільки скриптам, чий шлях починається із зазначеного рядка. Значення за промовчанням означає відсутність обмежень.

`opcache.file_update_protection` string

Запобігає кешування файлів молодше за вказану кількість секунд. Це допомагає запобігти кешуванням не до кінця оновлених файлів. У випадку, якщо у вас всі оновлення файлів атомарні, можна підвищити продуктивність, задавши цей параметр рівним "0".

`opcache.huge_code_pages` bool

Включає або вимикає копіювання коду PHP (текстового сегмента) у HUGE PAGES. Це може підвищити продуктивність, але потребує відповідних системних налаштувань. Доступно в Linux, починаючи з PHP 7.0.0 і FreeBSD, починаючи з PHP 7.4.0.

`opcache.lockfile_path` string

Абсолютний шлях до сховища спільних файлів блокувань (тільки nix)

`opcache.opt_debug_level` string

Здійснює виведення опкодів для налагодження різних етапів оптимізації. 0x10000 призведе до виведення опкодів як тільки вони згенеровані компілятором, до застосування будь-якої оптимізації. 0x20000 призведе до виведення опкодів після оптимізації.

`opcache.file_cache` string

Дозволяє та ставить директорію кеша другого рівня. Це має підвищити продуктивність, якщо пам'ять SHM заповнена, сервер перезапущено або SHM скинуто. Значення за промовчанням "" забороняє кешування на файловій системі.

`opcache.file_cache_only` bool

Включає або вимикає кешування опкодів у пам'яті, що розділяється.

> **Зауваження**
> 
> До PHP 8.1.0 відключення цієї директиви з вже заповненим файловим кешем вимагало ручного очищення файлового кешу.

`opcache.file_cache_consistency_checks` bool

Включає або вимикає перевірку контрольної суми під час завантаження скрипту з файлового кешу.

`opcache.file_cache_fallback` bool

Застосовує opcache.filecacheonly=1 для деяких процесів, які завершилися помилкою при перепідключенні до пам'яті, що розділяється (тільки для Windows). Потрібно явно дозволене кешування на файлову систему.

**Застереження**

Вимкнення цієї опції конфігурації може перешкодити запуску процесів, тому не рекомендується.

`opcache.validate_permission` bool

Перевірка прав доступу до кешованого файлу для поточного користувача.

`opcache.validate_root` bool

Запобігає колізії імен у chroot-оточенні. Повинне бути включено для всіх випадків використання chroot-оточень для запобігання доступу до файлів за межами chroot.

`opcache.preload` string

Задає скрипт PHP, який буде скомпілюваний і запущений при старті сервера і зможе завантажити інші файли, або за допомогою [include](function.include.html), або використовуючи функцію [opcache\_compile\_file()](function.opcache-compile-file.html). Усі сутності (наприклад, функції та класи), визначені в цих файлах, автоматично будуть доступні до моменту вимкнення сервера.

> **Зауваження**
> 
> Попереднє завантаження не підтримується у Windows.

`opcache.preload_user` string

Попереднє завантаження коду з правами root заборонено з міркувань безпеки. Ця директива полегшує запуск попереднього завантаження від імені іншого користувача.

`opcache.cache_id` string

У Windows всі процеси, що виконують той самий PHP SAPI під одним і тим же обліковим записом користувача з однаковим ідентифікатором кеша, спільно використовують один екземпляр OPcache. Значення ідентифікатора кешу можна вільно вибрати.

**Підказка**

Для IIS різні пули додатків можуть мати власний екземпляр OPcache, використовуючи змінне середовище APPPOOLID як `opcache.cache_id`

`opcache.jit` string|int

Для звичайного використання параметр приймає одне із чотирьох рядкових значень:

-   `disable`: Повністю вимкнено, не може бути увімкнено під час виконання.
-   `off`: Вимкнено, але може бути увімкнено під час виконання.
-   `tracing``on`: Використовуйте трасування JIT Увімкнено за промовчанням і рекомендується для більшості користувачів.
-   `function`: Використовуйте JIT.

Для розширеного використання параметр приймає 4-значне ціле число `CRTO`, де цифри означають:

`C` (Прапори оптимізації для процесора)

-   `0`: Вимкнути оптимізацію ЦП.
-   `1`: Увімкніть AVX, якщо ЦП підтримує його.

`R` (розподіл регістрів)

-   `0`: Не виконувати розподіл регістрів.
-   `1`: Виконувати виділення локального блокового регістру.
-   `2`: Виконувати виділення глобального регістру

`T` (тригер)

-   `0`: Компіляція всіх функцій під час завантаження скрипта.
-   `1`: Компіляція функцій під час першого виконання.
-   `2`: Профілювання функцій при першому запиті, а потім компілювання найпопулярніших функцій.
-   `3`: Профілювання на льоту та компіляція гарячих функцій.
-   `4`: В даний час не використовується.
-   `5`: Використання трасування JIT Профілювання на льоту та компіляція трасування для гарячих сегментів коду.

`O` (Рівень оптимізації)

-   `0`: Без JIT
-   `1`: Мінімальний JIT (виклик стандартних обробників віртуальних машин).
-   `2`: Вбудовані обробники віртуальних машин
-   `3`: Використовувати виведення типу.
-   `4`: Використовувати графік дзвінків.
-   `5`: Оптимізувати весь скрипт

Режим `"tracing"` відповідає `CRTO = 1254`, Режим `"function"` відповідає `CRTO = 1205`

`opcache.jit_buffer_size` int

Об'єм пам'яті, що розділяється, резервований для скомпільованого JIT-коду. Нульове значення вимикає JIT.

Якщо використовується int значення вимірюється байтами. Ви також можете використовувати скорочений запис, який описано в [этом разделе FAQ](faq.using.html#faq.using.shorthandbytes)

`opcache.jit_debug` int

Бітова маска, яка визначає, який висновок налагодження JIT слід увімкнути. Можливі значення дивіться у zendjit.h.

`opcache.jit_bisect_limit` int

Опція налагодження, що відключає JIT-компіляцію після компіляції певної кількості функцій. Може бути корисним для поділу джерела неправильної компіляції JIT. Примітка: цей параметр працює, тільки якщо для тригера JIT встановлено значення 0 (компіляція під час завантаження скрипта) або 1 (компіляція при першому виконанні), наприклад, `opcache.jit=1215`. Детальніше дивіться у розділі [opcache.jit](opcache.configuration.html#ini.opcache.jit)

`opcache.jit_prof_threshold` float

При використанні режиму тригера "профілювання функцій при першому запиті" цей поріг визначає, чи функція вважається гарячою. Кількість дзвінків функції, поділена на кількість дзвінків усіх функцій, повинна бути вищою за порогове значення. Наприклад, поріг 0,005 означає, що функції, що становлять понад 0,5% всіх викликів, будуть скомпільовані JIT.

`opcache.jit_max_root_traces` int

Максимальна кількість кореневих стеків виклику. Кореневий стек виклику - це потік виконання, що проходить за кодом спочатку одним шляхом, що є одиницею компіляції JIT. JIT не буде компілювати новий код, якщо він досягне цієї межі.

`opcache.jit_max_side_traces` int

Максимальна кількість бічних стеків виклику, які можуть мати кореневий стек. Бічний стек виклику - це інший потік виконання, який не слідує шляхом скомпілюваного кореневого стека виклику. Бічні стеки виклику, що належать одному і тому ж кореневому стеку виклику, не компілюватимуться, якщо вони досягають цієї межі.

`opcache.jit_max_exit_counters` int

Максимальна кількість лічильників виходу бокового стека виклику. Це обмежує загальну кількість бічних стеків, які можуть бути у всіх кореневих стеках.

`opcache.jit_hot_loop` int

Через скільки ітерацій цикл вважається гарячим. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких циклів.

`opcache.jit_hot_func` int

Через скільки дзвінків функція вважається гарячою. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких функцій.

`opcache.jit_hot_return` int

Через скільки повернень повернення вважається гарячим. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких повернень.

`opcache.jit_hot_side_exit` int

Через скільки виходів бічний стек вважається гарячим. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких побічних виходів.

`opcache.jit_blacklist_root_trace` int

Максимальна кількість спроб компіляції кореневого трасування, перш ніж вона буде занесена до чорного списку.

`opcache.jit_blacklist_side_trace` int

Максимальна кількість спроб компіляції бічного трасування до того, як вона буде занесена до чорного списку.

`opcache.jit_max_loop_unrolls` int

Максимальна кількість спроб розгорнути цикл у бічній трасуванні, намагаючись досягти кореневого трасування та закрити зовнішній цикл.

`opcache.jit_max_recursive_calls` int

Максимальна кількість розгорнутих рекурсивних циклів дзвінка.

`opcache.jit_max_recursive_returns` int

Максимальна кількість розгорнутих рекурсивних циклів повернення.

`opcache.jit_max_polymorphic_calls` int

Максимальна кількість спроб вбудованих поліморфних (динамічних чи методичних) викликів. Виклики вище за цей ліміт обробляються як метаморфічні і не вбудовуються.