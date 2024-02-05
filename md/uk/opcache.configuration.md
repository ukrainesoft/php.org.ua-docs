---
navigation:
  - opcache.installation.md: « Встановлення
  - opcache.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - opcache.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування OPcache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [opcache.enable](opcache.configuration.md#ini.opcache.enable) | "1" | **`INI_ALL`** |  |
| [opcache.enable\_cli](opcache.configuration.md#ini.opcache.enable-cli) | "0" | **`INI_SYSTEM`** | У версіях з PHP 7.1.2 до 7.1.6 включно, значення за замовчуванням "1" (включено) |
| [opcache.memory\_consumption](opcache.configuration.md#ini.opcache.memory-consumption) | "128" | **`INI_SYSTEM`** |  |
| [opcache.interned\_strings\_buffer](opcache.configuration.md#ini.opcache.interned-strings-buffer) | "8" | **`INI_SYSTEM`** |  |
| [opcache.max\_accelerated\_files](opcache.configuration.md#ini.opcache.max-accelerated-files) | "10000" | **`INI_SYSTEM`** |  |
| [opcache.max\_wasted\_percentage](opcache.configuration.md#ini.opcache.max-wasted-percentage) | "5" | **`INI_SYSTEM`** |  |
| [opcache.use\_cwd](opcache.configuration.md#ini.opcache.use-cwd) | "1" | **`INI_SYSTEM`** |  |
| [opcache.validate\_timestamps](opcache.configuration.md#ini.opcache.validate-timestamps) | "1" | **`INI_ALL`** |  |
| [opcache.revalidate\_freq](opcache.configuration.md#ini.opcache.revalidate-freq) | "2" | **`INI_ALL`** |  |
| [opcache.revalidate\_path](opcache.configuration.md#ini.opcache.revalidate-path) | "0" | **`INI_ALL`** |  |
| [opcache.save\_comments](opcache.configuration.md#ini.opcache.save-comments) | "1" | **`INI_SYSTEM`** |  |
| [opcache.fast\_shutdown](opcache.configuration.md#ini.opcache.fast-shutdown) | "0" | **`INI_SYSTEM`** |  |
| [opcache.enable\_file\_override](opcache.configuration.md#ini.opcache.enable-file-override) | "0" | **`INI_SYSTEM`** |  |
| [opcache.optimization\_level](opcache.configuration.md#ini.opcache.optimization-level) | "0x7FFEBFFF" | **`INI_SYSTEM`** | До PHP 7.3.0 було 0x7FFFBFFF |
| [opcache.inherited\_hack](opcache.configuration.md#ini.opcache.inherited-hack) | "1" | **`INI_SYSTEM`** | Вилучено у PHP 7.3.0 |
| [opcache.dups\_fix](opcache.configuration.md#ini.opcache.dups-fix) | "0" | **`INI_ALL`** |  |
| [opcache.blacklist\_filename](opcache.configuration.md#ini.opcache.blacklist-filename) | "" | **`INI_SYSTEM`** |  |
| [opcache.max\_file\_size](opcache.configuration.md#ini.opcache.max-file-size) | "0" | **`INI_SYSTEM`** |  |
| [opcache.consistency\_checks](opcache.configuration.md#ini.opcache.consistency-checks) | "0" | **`INI_ALL`** | Недоступно з PHP 8.1.18 та 8.2.5. Вилучено у PHP 8.3.0. |
| [opcache.force\_restart\_timeout](opcache.configuration.md#ini.opcache.force-restart-timeout) | "180" | **`INI_SYSTEM`** |  |
| [opcache.error\_log](opcache.configuration.md#ini.opcache.error-log) | "" | **`INI_SYSTEM`** |  |
| [opcache.log\_verbosity\_level](opcache.configuration.md#ini.opcache.log-verbosity-level) | "1" | **`INI_SYSTEM`** |  |
| [opcache.record\_warnings](opcache.configuration.md#ini.opcache.record-warnings) | "0" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0. |
| [opcache.preferred\_memory\_model](opcache.configuration.md#ini.opcache.preferred-memory-model) | "" | **`INI_SYSTEM`** |  |
| [opcache.protect\_memory](opcache.configuration.md#ini.opcache.protect-memory) | "0" | **`INI_SYSTEM`** |  |
| [opcache.mmap\_base](opcache.configuration.md#ini.opcache.mmap-base) | **`null`** | **`INI_SYSTEM`** |  |
| [opcache.restrict\_api](opcache.configuration.md#ini.opcache.restrict-api) | "" | **`INI_SYSTEM`** |  |
| [opcache.file\_update\_protection](opcache.configuration.md#ini.opcache.file_update_protection) | "2" | **`INI_ALL`** |  |
| [opcache.huge\_code\_pages](opcache.configuration.md#ini.opcache.huge_code_pages) | "0" | **`INI_SYSTEM`** |  |
| [opcache.lockfile\_path](opcache.configuration.md#ini.opcache.lockfile_path) | "/tmp" | **`INI_SYSTEM`** |  |
| [opcache.opt\_debug\_level](opcache.configuration.md#ini.opcache.opt_debug_level) | "0" | **`INI_SYSTEM`** | Доступно з PHP 7.1.0 |
| [opcache.file\_cache](opcache.configuration.md#ini.opcache.file-cache) | NULL | **`INI_SYSTEM`** |  |
| [opcache.file\_cache\_only](opcache.configuration.md#ini.opcache.file-cache-only) | "0" | **`INI_SYSTEM`** |  |
| [opcache.file\_cache\_consistency\_checks](opcache.configuration.md#ini.opcache.file-cache-consistency-checks) | "1" | **`INI_SYSTEM`** |  |
| [opcache.file\_cache\_fallback](opcache.configuration.md#ini.opcache.file-cache-fallback) | "1" | **`INI_SYSTEM`** |  |
| [opcache.validate\_permission](opcache.configuration.md#ini.opcache.validate-permission) | "0" | **`INI_SYSTEM`** | Доступно з PHP 7.0.14 |
| [opcache.validate\_root](opcache.configuration.md#ini.opcache.validate-root) | "0" | **`INI_SYSTEM`** | Доступно з PHP 7.0.14 |
| [opcache.preload](opcache.configuration.md#ini.opcache.preload) | "" | **`INI_SYSTEM`** | Доступно з PHP 7.4.0 |
| [opcache.preload\_user](opcache.configuration.md#ini.opcache.preload-user) | "" | **`INI_SYSTEM`** | Доступно з PHP 7.4.0 |
| [opcache.cache\_id](opcache.configuration.md#ini.opcache.cache-id) | "" | **`INI_SYSTEM`** | Тільки Windows. Доступно з PHP 7.4.0 |
| [opcache.jit](opcache.configuration.md#ini.opcache.jit) | "tracing" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_buffer\_size](opcache.configuration.md#ini.opcache.jit-buffer-size) | "0" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_debug](opcache.configuration.md#ini.opcache.jit-debug) | "0" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_bisect\_limit](opcache.configuration.md#ini.opcache.jit-bisect-limit) | "0" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_prof\_threshold](opcache.configuration.md#ini.opcache.jit-prof-threshold) | "0.005" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_root\_traces](opcache.configuration.md#ini.opcache.jit-max-root-traces) | "1024" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_side\_traces](opcache.configuration.md#ini.opcache.jit-max-side-traces) | "128" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_exit\_counters](opcache.configuration.md#ini.opcache.jit-max-exit-counters) | "8192" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_loop](opcache.configuration.md#ini.opcache.jit-hot-loop) | "64" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_func](opcache.configuration.md#ini.opcache.jit-hot-func) | "127" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_return](opcache.configuration.md#ini.opcache.jit-hot-return) | "8" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_hot\_side\_exit](opcache.configuration.md#ini.opcache.jit-hot-side-exit) | "8" | **`INI_SYSTEM`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_blacklist\_root\_trace](opcache.configuration.md#ini.opcache.jit-blacklist-root-trace) | "16" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_blacklist\_side\_trace](opcache.configuration.md#ini.opcache.jit-blacklist-side-trace) | "8" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_loop\_unrolls](opcache.configuration.md#ini.opcache.jit-max-loop-unrolls) | "8" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_recursive\_calls](opcache.configuration.md#ini.opcache.jit-max-recursive-calls) | "2" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_recursive\_returns](opcache.configuration.md#ini.opcache.jit-max-recursive-return) | "2" | **`INI_ALL`** | Доступно з PHP 8.0.0 |
| [opcache.jit\_max\_polymorphic\_calls](opcache.configuration.md#ini.opcache.jit-max-polymorphic-calls) | "2" | **`INI_ALL`** | Доступно з PHP 8.0.0 |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`opcache.enable`bool

Дозволяє кешування опкодів. Якщо заборонено, код не оптимізуватиметься і не кешуватиметься. Опцію `opcache.enable` не можна увімкнути під час виконання за допомогою [ini\_set()](function.ini-set.md), але можна вимкнути. Спроба включити її у такий спосіб призведе до генерації попередження.

`opcache.enable_cli`bool

Дозволяє кешування опкодів для CLI-версії PHP.

`opcache.memory_consumption`int

Размер разделяемой памяти в мегабайтах для OPcache. Минимально допустимое значение —`"8"`, яке застосовується, якщо встановлено менше значення.

`opcache.interned_strings_buffer`int

Кількість пам'яті в мегабайтах для зберігання інтернованих рядків.

`opcache.max_accelerated_files`int

Максимальна кількість ключів (і, відповідно, скриптів) у хеш-таблиці OPcache. Фактичне значення буде першим числом з набору `{ 223, 463, 983, 1979, 3907, 7963, 16229, 32531, 65407, 130987, 262237, 524521, 1048793 }`, яке більше або дорівнює заданому в цьому параметрі. Мінімум 200, максимум 1000000. Значення за межами діапазону обмежені до допустимого діапазону.

`opcache.max_wasted_percentage`int

Максимальне значення втраченої пам'яті (у відсотках) після якого планується перезапуск, якщо недостатньо вільної пам'яті. Максимально допустиме значення: `"50"`, яка застосовується, якщо встановлено більше значення.

`opcache.use_cwd`bool

Якщо увімкнено, OPcache додає поточну робочу директорію до ключа скрипту, тим самим усуваючи можливість колізій для файлів з однаковим ім'ям. Вимкнення цієї опції підвищує продуктивність, але може призвести до збоїв.

`opcache.validate_timestamps`bool

Якщо увімкнено, OPcache перевірятиме актуальність закешованих скриптів кожні [opcache.revalidate\_freq](opcache.configuration.md#ini.opcache.revalidate-freq) секунд. Коли заборонено, ви можете перезапустити OPcache вручну за допомогою [opcache\_reset()](function.opcache-reset.md) [opcache\_invalidate()](function.opcache-invalidate.md) або перезапустити веб-сервер для того, щоб зміни набули чинності.

> **Зауваження**: OPcache все ще може перевіряти тимчасову мітку файлу під час компіляції, якщо для опцій [opcache.file\_update\_protection](opcache.configuration.md#ini.opcache.file_update_protection) або [opcache.max\_file\_size](opcache.configuration.md#ini.opcache.max-file-size) встановлені ненульові значення.

`opcache.revalidate_freq`int

Як часто в секундах перевіряти тимчасові мітки файлів . призведе до того, що OPcache проводитиме цю перевірку при кожному запиті.

Ця директива ігнорується, якщо вимкнено [opcache.validate\_timestamps](opcache.configuration.md#ini.opcache.validate-timestamps)

`opcache.revalidate_path`bool

Якщо вимкнено, існуючі закешовані файли, які використовують один і той же [include\_path](ini.core.md#ini.include-path), повторно використовуватимуться. Таким чином, якщо файл з тим же ім'ям знаходиться в іншому місці в include\_path, його не буде знайдено.

`opcache.save_comments`bool

Якщо вимкнено, всі коментарі будуть відкинуті з кешу опкодів для мінімізації розміру коду. Відключення цієї опції може призвести до того, що деякі фреймворки, що покладаються на анотації в коментарях, перестануть працювати, включаючи Doctrine, Zend Framework 2 та PHPUnit.

`opcache.fast_shutdown`bool

Якщо увімкнено, то буде використана швидка послідовність перезавантаження, при якій не відбувається очищення всіх виділених блоків пам'яті. Натомість для звільнення всього набору змінних використовується стандартний менеджер пам'яті Zend Engine.

Ця директива була видалена у PHP 7.2.0. Варіант швидкої послідовності перезавантаження був інтегрований у PHP і автоматично використовуватиметься, якщо це можливо.

`opcache.enable_file_override`bool

Якщо увімкнено, то кеш опкодів перевірятиме, чи вже закешовано файл при викликі функцій [file\_exists()](function.file-exists.md) [is\_file()](function.is-file.md) і [is\_readable()](function.is-readable.md). Це може підвищити продуктивність додатків, які перевіряють присутність і доступність для читання скриптом PHP, але несе ризик повернення застарілих даних, якщо заборонена опція [opcache.validate\_timestamps](opcache.configuration.md#ini.opcache.validate-timestamps)

`opcache.optimization_level`int

Бітова маска, яка контролює, які кроки оптимізації виконуються. За промовчанням застосовуються всі безпечні оптимізації. Зміна значення за промовчанням корисна для налагодження/розробки оптимізатора (див. також [opcache.opt\_debug\_level](opcache.configuration.md#ini.opcache.opt_debug_level)

`opcache.inherited_hack`bool

Ця директива ігнорується.

`opcache.dups_fix`bool

Цей хак потрібний лише для обходу помилок "Cannot redeclare class".

`opcache.blacklist_filename`string

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

`opcache.max_file_size`int

Максимальний розмір файлу для кешування у байтах. Якщо поставити , то кешуватимуться всі файли.

`opcache.consistency_checks`int

Якщо не нуль, OPcache звірятиме контрольну суму кешу кожні N запитів, де N — задане в цій директиві значення. Рекомендується включати лише при налагодженні, оскільки сильно впливає на продуктивність.

> **Зауваження** :
> 
> Недоступно з PHP 8.1.18 та 8.2.5. Вилучено у PHP 8.3.0.

`opcache.force_restart_timeout`int

Кількість секунд очікування звільнення кеша, після якого буде примусово здійснено запланований перезапуск. Якщо цей час перевищено, OPcache вважає, що відбувається щось неправильне і вбиває процес блокування кешу.

Якщо параметр [opcache.log\_verbosity\_level](opcache.configuration.md#ini.opcache.log-verbosity-level) задати рівним 2 або більше, то, при виникненні такої ситуації, у лог помилок буде записано попередження.

Директива не підтримується у Windows.

`opcache.error_log`string

Лог помилок OPcache. Порожній рядок вважається як `stderr`і помилки будуть виведені в стандартний потік помилок (у більшості випадків це лог помилок веб-сервера).

`opcache.log_verbosity_level`int

Рівень подробиці помилок лога. За умовчанням записуватимуться лише фатальні помилки (рівень 0) та помилки (рівень 1). Також значення можуть бути такими: попередження (рівень 2), інформаційні повідомлення (рівень 3) та повідомлення налагодження (рівень 4).

`opcache.record_warnings`bool

Якщо увімкнено, OPcache запише попередження під час компіляції та відтворить їх при наступному увімкненні, навіть якщо воно виконується з кеша.

`opcache.preferred_memory_model`string

Вподобана модель пам'яті для OPcache. Якщо залишити порожнім, то OPcache самостійно вибере найбільш підходящу модель, яка поводитиметься коректно практично у будь-яких випадках.

Можливі значення включають `mmap` `shm` `posix`и`win32`

`opcache.protect_memory`bool

Захищає пам'ять від несподіваного запису під час запуску скриптів. Корисно тільки для внутрішнього налагодження.

`opcache.mmap_base`string

Базове значення для сегмента пам'яті, що розділяється в Windows. Всі процеси PHP повинні відображати пам'ять, що розділяється, в однаковий адресний простір. Ця опція допомагає полагодити помилки типу "Unable to reattach to base address".

`opcache.restrict_api`string

Дозволяє викликати функції API OPcache лише скриптам, чий шлях починається із зазначеного рядка. Значення за промовчанням означає відсутність обмежень.

`opcache.file_update_protection`string

Виключить кешування файлів з моменту зміни яких пройшло менше секунд, ніж зазначено. Це захищає від кешування не повністю оновлених файлів. Якщо всі оновлення файлів атомарні, можна підвищити продуктивність, задавши цей параметр рівним . Це дозволить закешувати файли негайно.

`opcache.huge_code_pages`bool

Включає або вимикає копіювання коду PHP (текстового сегмента) у HUGE PAGES. Це може підвищити продуктивність, але потребує відповідних системних налаштувань. Доступно в Linux, починаючи з PHP 7.0.0 і FreeBSD, починаючи з PHP 7.4.0.

`opcache.lockfile_path`string

Абсолютний шлях до спільного сховища файлів блокування (лише \*nix)

`opcache.opt_debug_level`string

Виводить код операції для налагодження різних етапів оптимізації. 0x10000 призведе до виведення кодів операцій, щойно їх згенерує компілятор, перш ніж буде застосовано будь-яку оптимізацію. 0x20000 спричинить виведення кодів операцій після оптимізації.

`opcache.file_cache`string

Дозволяє та ставить директорію кеша другого рівня. Це має підвищити продуктивність, якщо пам'ять SHM заповнена, сервер перезапущено або SHM скинуто. Значення за промовчанням "" забороняє кешування на файловій системі.

`opcache.file_cache_only`bool

Включає або вимикає кешування опкодів у пам'яті, що розділяється.

> **Зауваження** :
> 
> До PHP 8.1.0 відключення цієї директиви з вже заповненим файловим кешем вимагало ручного очищення файлового кешу.

`opcache.file_cache_consistency_checks`bool

Включає або вимикає перевірку контрольної суми під час завантаження скрипта з файлового кешу.

`opcache.file_cache_fallback`bool

Застосовує opcache.file\_cache\_only=1 для деяких процесів, які завершилися помилкою при перепідключенні до пам'яті, що розділяється (тільки для Windows). Потрібно явно дозволене кешування на файлову систему.

**Застереження**

Вимкнення цієї опції конфігурації може перешкодити запуску процесів, тому не рекомендується.

`opcache.validate_permission`bool

Перевірка прав доступу до кешованого файлу для поточного користувача.

`opcache.validate_root`bool

Запобігає колізії імен у chroot-оточенні. Повинне бути включено для всіх випадків використання chroot-оточень для запобігання доступу до файлів за межами chroot.

`opcache.preload`string

Задає скрипт PHP, який буде скомпільований і запущений при старті сервера і зможе завантажити інші файли, або за допомогою [include](function.include.md), либо используя функцию[opcache\_compile\_file()](function.opcache-compile-file.md). Усі сутності (наприклад, функції та класи), визначені в цих файлах, автоматично будуть доступні до моменту вимкнення сервера.

> **Зауваження** :
> 
> Попереднє завантаження не підтримується у Windows.

`opcache.preload_user`string

Дозволяє запускати попереднє завантаження від імені вказаного користувача системи. Корисно для серверів, які запускаються від імені root перед перемиканням на непривілейованого користувача системи. За промовчанням попереднє завантаження від імені root заборонено з міркувань безпеки, якщо тільки цій директиві явно не встановлено значення `root`

`opcache.cache_id`string

У Windows всі процеси, що виконують той самий PHP SAPI під одним і тим же обліковим записом користувача з однаковим ідентифікатором кеша, спільно використовують один екземпляр OPcache. Значення ідентифікатора кешу можна вільно вибрати.

**Підказка**

Для IIS різні пули додатків можуть мати власний екземпляр OPcache, використовуючи змінне середовище APP\_POOL\_ID як `opcache.cache_id`

`opcache.jit`string|int

Для звичайного використання параметр приймає одне із чотирьох рядкових значень:

-   `disable`: Повністю вимкнено, не може бути увімкнено під час виконання.
-   `off`: Вимкнено, але може бути увімкнено під час виконання.
-   `tracing` `on`: Використовуйте трасування JIT Увімкнено за промовчанням і рекомендується для більшості користувачів.
-   `function`: Використовуйте JIT.

Для розширеного використання параметр приймає 4-значне ціле число `CRTO`, де цифри означають:

`C`(Флаги оптимизации для процессора)

-   : Вимкнути оптимізацію ЦП.
-   : Увімкніть AVX, якщо ЦП підтримує його.

`R`(распределение регистров)

-   : Не виконувати розподіл регістрів.
-   : Виконувати виділення локального блокового регістру.
-   : Виконувати виділення глобального регістру

`T`(триггер)

-   : Компіляція всіх функцій під час завантаження скрипта.
-   : Компіляція функцій під час першого виконання.
-   : Профільування функцій при першому запиті, а потім компілювання найпопулярніших функцій.
-   `3`: Профілювання на льоту та компіляція гарячих функцій.
-   `4`: В даний час не використовується.
-   `5`: Використання трасування JIT Профілювання на льоту та компіляція трасування для гарячих сегментів коду.

`O`(уровень оптимизации)

-   : Без JIT
-   : Мінімальний JIT (виклик стандартних обробників віртуальних машин).
-   : Вбудовані обробники віртуальних машин
-   `3`: Використовувати виведення типу.
-   `4`: Використовувати графік дзвінків.
-   `5`: Оптимізувати весь скрипт

Режим`"tracing"` відповідає `CRTO = 1254`, Режим`"function"` відповідає `CRTO = 1205`

`opcache.jit_buffer_size`int

Об'єм пам'яті, що розділяється, резервований для скомпільованого JIT-коду. Нульове значення вимикає JIT.

Якщо вказано ціле значення (int), обсяг вимірюється байтами. Можна також використовувати скорочений запис, який описано в [у цьому розділі FAQ](faq.using.md#faq.using.shorthandbytes)

`opcache.jit_debug`int

Бітова маска, яка визначає, який висновок налагодження JIT слід увімкнути. Можливі значення дивіться у файлі [» zend\_jit.h](https://github.com/php/php-src/blob/master/ext/opcache/jit/zend_jit.h) (Пошук макровизначень, що починаються з `ZEND_JIT_DEBUG`

`opcache.jit_bisect_limit`int

Опція налагодження, що відключає JIT-компіляцію після компіляції певної кількості функцій. Може бути корисним для поділу джерела неправильної компіляції JIT. Примітка: цей параметр працює, тільки якщо для тригера JIT встановлено значення 0 (компіляція під час завантаження скрипта) або 1 (компіляція при першому виконанні), наприклад, `opcache.jit=1215`Подробнее смотрите в разделе[opcache.jit](opcache.configuration.md#ini.opcache.jit)

`opcache.jit_prof_threshold`float

При використанні режиму тригера "профілювання функцій при першому запиті" цей поріг визначає, чи функція вважається гарячою. Кількість дзвінків функції, поділена на кількість дзвінків усіх функцій, повинна бути вищою від порогового значення. Наприклад, поріг 0,005 означає, що функції, що становлять більше ніж 0,5% всіх викликів, будуть скомпільовані JIT.

`opcache.jit_max_root_traces`int

Максимальна кількість кореневих стеків виклику. Кореневий стек виклику - це потік виконання, що проходить за кодом спочатку одним шляхом, що є одиницею компіляції JIT. JIT не буде компілювати новий код, якщо він досягне цієї межі.

`opcache.jit_max_side_traces`int

Максимальна кількість бічних стеків виклику, які можуть мати кореневий стек. Бічний стек виклику - це інший потік виконання, який не слідує шляхом скомпілюваного кореневого стека виклику. Бічні стеки виклику, що належать одному і тому ж кореневому стеку виклику, не компілюватимуться, якщо вони досягають цієї межі.

`opcache.jit_max_exit_counters`int

Максимальна кількість лічильників виходу бокового стека виклику. Це обмежує загальну кількість бічних стеків, які можуть бути у всіх кореневих стеках.

`opcache.jit_hot_loop`int

Через скільки ітерацій цикл вважається гарячим. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких циклів.

`opcache.jit_hot_func`int

Через скільки дзвінків функція вважається гарячою. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких функцій.

`opcache.jit_hot_return`int

Через скільки повернень повернення вважається гарячим. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких повернень.

`opcache.jit_hot_side_exit`int

Через скільки виходів бічний стек вважається гарячим. Допустимий діапазон значень: `[0,255]`; для будь-якого значення поза цим діапазоном, наприклад -1 або 256, буде використовуватися значення за замовчуванням. Зокрема, нульове значення відключить JIT для відстеження та компіляції будь-яких побічних виходів.

`opcache.jit_blacklist_root_trace`int

Максимальна кількість спроб компіляції кореневого трасування, перш ніж вона буде занесена до чорного списку.

`opcache.jit_blacklist_side_trace`int

Максимальна кількість спроб компіляції бокового трасування до того, як вона буде занесена до чорного списку.

`opcache.jit_max_loop_unrolls`int

Максимальна кількість спроб розгорнути цикл у бічній трасуванні, намагаючись досягти кореневого трасування та закрити зовнішній цикл.

`opcache.jit_max_recursive_calls`int

Максимальна кількість розгорнутих рекурсивних циклів дзвінка.

`opcache.jit_max_recursive_returns`int

Максимальна кількість розгорнутих рекурсивних циклів повернення.

`opcache.jit_max_polymorphic_calls`int

Максимальна кількість спроб вбудованих поліморфних (динамічних чи методичних) викликів. Виклики вище за цей ліміт обробляються як метаморфічні і не вбудовуються.
