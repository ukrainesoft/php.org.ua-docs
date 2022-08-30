Налаштування під час виконання

-   [« Установка](session.installation.md)
    
-   [Типи ресурсів »](session.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](session.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування механізму сесій**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [session.savepath](session.configuration.html#ini.session.save-path) | "" | PHPINIALL |  |
| [session.name](session.configuration.html#ini.session.name) | "PHPSESSID" | PHPINIALL |  |
| [session.savehandler](session.configuration.html#ini.session.save-handler) | "files" | PHPINIALL |  |
| [session.autostart](session.configuration.html#ini.session.auto-start) | "0" | PHPINIPERDIR |  |
| [session.gcprobability](session.configuration.html#ini.session.gc-probability) | "1" | PHPINIALL |  |
| [session.gcdivisor](session.configuration.html#ini.session.gc-divisor) | "100" | PHPINIALL |  |
| [session.gcmaxlifetime](session.configuration.html#ini.session.gc-maxlifetime) | "1440" | PHPINIALL |  |
| [session.serializehandler](session.configuration.html#ini.session.serialize-handler) | "php" | PHPINIALL |  |
| [session.cookielifetime](session.configuration.html#ini.session.cookie-lifetime) | "0" | PHPINIALL |  |
| [session.cookiepath](session.configuration.html#ini.session.cookie-path) | "/" | PHPINIALL |  |
| [session.cookiedomain](session.configuration.html#ini.session.cookie-domain) | "" | PHPINIALL |  |
| [session.cookiesecure](session.configuration.html#ini.session.cookie-secure) | "0" | PHPINIALL | До PHP 7.2.0 значення за промовчанням було `""` |
| [session.cookiehttponly](session.configuration.html#ini.session.cookie-httponly) | "0" | PHPINIALL | До PHP 7.2.0 значення за промовчанням було `""` |
| [session.cookiesamesite](session.configuration.html#ini.session.cookie-samesite) | "" | PHPINIALL | Доступна з PHP 7.3.0. |
| [session.usestrictmode](session.configuration.html#ini.session.use-strict-mode) | "0" | PHPINIALL |  |
| [session.usecookies](session.configuration.html#ini.session.use-cookies) | "1" | PHPINIALL |  |
| [session.useonlycookies](session.configuration.html#ini.session.use-only-cookies) | "1" | PHPINIALL |  |
| [session.referercheck](session.configuration.html#ini.session.referer-check) | "" | PHPINIALL |  |
| [session.cachelimiter](session.configuration.html#ini.session.cache-limiter) | "nocache" | PHPINIALL |  |
| [session.cacheexpire](session.configuration.html#ini.session.cache-expire) | "180" | PHPINIALL |  |
| [session.usetranssid](session.configuration.html#ini.session.use-trans-sid) | "0" | PHPINIALL |  |
| [session.transsidtags](session.configuration.html#ini.session.trans-sid-tags) | "a=href,area=href,frame=src,form=" | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.transsidhosts](session.configuration.html#ini.session.trans-sid-hosts) | `$_SERVER['HTTP_HOST']` | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.sidlength](session.configuration.html#ini.session.sid-length) | "32" | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.sidbitspercharacter](session.configuration.html#ini.session.sid-bits-per-character) | "4" | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.uploadprogress.enabled](session.configuration.html#ini.session.upload-progress.enabled) | "1" | PHPINIPERDIR |  |
| [session.uploadprogress.cleanup](session.configuration.html#ini.session.upload-progress.cleanup) | "1" | PHPINIPERDIR |  |
| [session.uploadprogress.prefix](session.configuration.html#ini.session.upload-progress.prefix) | "uploadprogress" | PHPINIPERDIR |  |
| [session.uploadprogress.name](session.configuration.html#ini.session.upload-progress.name) | "PHPSESSIONUPLOADPROGRESS" | PHPINIPERDIR |  |
| [session.uploadprogress.freq](session.configuration.html#ini.session.upload-progress.freq) | "1%" | PHPINIPERDIR |  |
| [session.uploadprogress.minfreq](session.configuration.html#ini.session.upload-progress.min-freq) | "1" | PHPINIPERDIR |  |
| [session.lazywrite](session.configuration.html#ini.session.lazy-write) | "1" | PHPINIALL |  |
| [session.hashfunction](session.configuration.html#ini.session.hash-function) | "0" | PHPINIALL | Видалено в PHP 7.1.0. |
| [session.hashbitspercharacter](session.configuration.html#ini.session.hash-bits-per-character) | "4" | PHPINIALL | Видалено в PHP 7.1.0. |
| [session.entropyfile](session.configuration.html#ini.session.entropy-file) | "" | PHPINIALL | Видалено в PHP 7.1.0. |
| [session.entropylength](session.configuration.html#ini.session.entropy-length) | "0" | PHPINIALL | Видалено в PHP 7.1.0 |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Система керування сесіями підтримує низку опцій, які можуть бути вказані у файлі php.ini. Нижче наведено короткий огляд.

`session.save_handler` string

`session.save_handler` визначає ім'я оброблювача, який використовується для зберігання та вилучення даних, пов'язаних із сесією. За замовчуванням має значення `files`. Слід звернути увагу на те, що деякі модулі можуть зареєструвати власні обробники (`save_handler`). Поточні зареєстровані обробники відображаються в [phpinfo()](function.phpinfo.md). Дивіться також [sessionsetsavehandler()](function.session-set-save-handler.html)

`session.save_path` string

`session.save_path` визначає аргумент, який передається до обробника збереження. При встановленому за замовчуванням обробнику files аргумент містить шлях, де будуть створюватися файли. Дивіться також [sessionsavepath()](function.session-save-path.html)

Ця директива також має додатковий аргумент `N`, Який визначає глибину розміщення файлів сесії щодо зазначеної директорії Наприклад, вказівка `'5;/tmp'` може зрештою призвести до такого розміщення файлу сесії: `/tmp/4/b/1/e/3/sess_4b1e384ad74619bd212e236e52a5a174If` . Для того, щоб використати аргумент `N`необхідно попередньо створити всі ці директорії. Допомогти цьому може невеликий скрипт, розташований в ext/session. Версія для bash називається modfiles.sh, а Windows-версія – modfiles.bat. Також слід враховувати, що якщо `N` визначено і більше 0, то автоматичне складання сміття не виконується, докладніше дивіться інформацію у файлі php.ini. Крім того, якщо використовується `N`, необхідно переконатися, що значення `session.save_path` вказано в лапках, оскільки роздільник (`;`) у php.ini використовується як знак коментаря.

Модуль зберігання файлів створює файли з правами 600 за промовчанням. Це можна змінити за допомогою необов'язкового аргументу `MODE` `N;MODE;/path`, де `MODE` - вісімкове представлення режиму доступу до файлу. Встановлення `MODE` не торкається umask.

**Увага**

Якщо встановити значення загальнодоступну для читання директорію, наприклад, /tmp (за замовчуванням), решта користувачів сервера отримають можливість перехопити сесію користувача, отримавши список файлів такої директорії.

**Застереження**

При використанні необов'язкового аргументу `N` рівня директорій, як описано вище, врахуйте, що використання значень вище ніж 1 або 2 неприпустимо для більшості сайтів, так як потрібно дуже багато директорій: наприклад, значення 3 призводить до `(2 ** session.sid_bits_per_character) ** 3` директоріям у файловій системі, які призводять до величезних втрат місця та inode.

Використовуйте тільки `N` більше 2, якщо ви абсолютно впевнені, що ваш сайт досить великий, щоб вимагати цього.

`session.name` string

`session.name` визначає назву сесії, яка використовується як назва cookies. Може містити лише цифри та літери. За замовчуванням одно `PHPSESSID`. Дивіться також [sessionname()](function.session-name.html)

`session.auto_start` bool

`session.auto_start` визначає, чи модуль сесії запускатиме сесію автоматично при старті. Значення за замовчуванням `0` (Вимкнено).

`session.serialize_handler` string

`session.serialize_handler` визначає ім'я оброблювача, який використовується для серіалізації/десеріалізації даних. Підтримується формат серіалізації PHP (найменування `php_serialize`), внутрішній формат PHP (найменування `php` і `php_binary`) та WDDX (найменування `wddx`). WDDX доступний тільки в тому випадку, якщо PHP скомпільовано з [підтримкою WDDX](ref.wddx.md). . `php_serialize` використовує просту функцію серіалізації/десеріалізації для внутрішніх потреб і не має тих обмежень, які є у `php` і `php_binary`. Старі обробники серіалізації не можуть зберігати ні числові, ні рядкові індекси, що містять спеціальні символи (`|` і `!`) у $SESSION. Використовуйте `php_serialize`, щоб уникнути помилок числових і рядкових індексів при завершенні скрипта. Значення за замовчуванням `php`

`session.gc_probability` int

`session.gc_probability` у поєднанні з `session.gc_divisor` визначає ймовірність запуску функції збирача сміття (gc, garbage collection). За замовчуванням дорівнює `1`. Дивіться докладніше у [session.gcdivisor](session.configuration.html#ini.session.gc-divisor)

`session.gc_divisor` int

`session.gc_divisor` у поєднанні з `session.gc_probability` визначає можливість запуску функції збирача сміття (gc, garbage collection) при кожній ініціалізації сесії. Імовірність розраховується як gcprobability/gcdivisor, тобто 1/100 означає, що функція gc запускається в одному випадку зі ста, або 1% при кожному запиті . `session.gc_divisor` за замовчуванням має значення `100`

`session.gc_maxlifetime` int

`session.gc_maxlifetime` задає відстрочку часу в секундах, після якої дані будуть розглядатися як "сміття" та потенційно будуть видалені. Збір сміття може відбутися протягом старту сесії (залежно від значень [session.gcprobability](session.configuration.html#ini.session.gc-probability) і [session.gcdivisor](session.configuration.html#ini.session.gc-divisor)). За замовчуванням значення `1440` (24 хвилини).

> **Зауваження**: Якщо різні скрипти мають різні значення `session.gc_maxlifetime`Але при цьому одні й ті ж місця для зберігання даних сесії, то скрипт з мінімальним значенням знищить усі дані. У такому разі слід використовувати цю директиву разом з [session.savepath](session.configuration.html#ini.session.save-path)

`session.referer_check` string

`session.referer_check` містить підрядок, який можна використовувати під час перевірки HTTP Referer. Якщо клієнтом був надісланий referer і підрядок не був виявлений, то ідентифікатор сесії буде позначений як недійсний. За промовчанням використовується порожній рядок.

`session.entropy_file` string

`session.entropy_file` містить шлях до ресурсу (файлу), що використовується як додаткове джерело ентропії у процесі створення ідентифікатора сесії. Наприклад, `/dev/random` або `/dev/urandom`, які доступні на багатьох Unix-системах. Ця можливість також підтримується у Windows. Вказівка ​​ненульового значення в `session.entropy_length` наказує PHP використовувати як джерело ентропії Windows Random API.

> **Зауваження**: Видалено в PHP 7.1.0 . `session.entropy_file` має значення за умовчанням рівне `/dev/urandom` або `/dev/arandom`якщо вони доступні.

`session.entropy_length` int

`session.entropy_length` визначає кількість байт, які будуть прочитані з вказаного вище файлу. За замовчуванням `32`. Вилучено у PHP 7.1.0.

`session.use_strict_mode` bool

`session.use_strict_mode` визначає, чи буде модуль використовувати режим суворого ідентифікатора (ID). Якщо від браузера отримано невизначений ID, браузеру буде надіслано новий ID. Таким чином, програми захищаються від фіксації сесії за допомогою суворого режиму. За замовчуванням `0` (Вимкнено).

> **Зауваження**: Включення `session.use_strict_mode` є обов'язковим для спільної безпеки сесії. Всім сайтам рекомендується її вмикати. Дивіться приклади [sessioncreateid()](function.session-create-id.html)

**Увага**

Якщо користувальницький обробник сесії, зареєстрований за допомогою [sessionsetsavehandler()](function.session-set-save-handler.html), не реалізує [SessionUpdateTimestampHandlerInterface::validateId()](sessionupdatetimestamphandlerinterface.validateid.md) та не надає callback-функцію `validate_sid`відповідно, режим суворого ідентифікатора сесії буде відключений, незалежно від значення цієї директиви. Особливо зверніть увагу, що [SessionHandler](class.sessionhandler.md) *не* реалізує **SessionHandler::validateId()**

`session.use_cookies` bool

`session.use_cookies` визначає, чи модуль використовуватиме cookies для зберігання ідентифікатора сесії на стороні клієнта. За замовчуванням `1` (Включено).

`session.use_only_cookies` bool

`session.use_only_cookies` визначає, чи модуль використовуватиме *тільки* cookies для зберігання сесії ідентифікатора на стороні клієнта. Увімкнення цього параметра запобігає атакам з використанням ідентифікатора сесії, розміщеного в URL. Значення за замовчуванням `1` (Включено).

`session.cookie_lifetime` int

`session.cookie_lifetime` вказує час життя cookies, що надсилається до браузера клієнта, в секундах. Значення 0 означає, що cookies будуть валідними до закриття браузера. За замовчуванням одно `0`. Дивіться також [sessiongetcookieparams()](function.session-get-cookie-params.html) і [sessionsetcookieparams()](function.session-set-cookie-params.html)

> **Зауваження**: Позначка закінчення часу встановлюється по відношенню до серверного часу, який не обов'язково збігається з часом у браузері клієнта.

`session.cookie_path` string

`session.cookie_path` визначає встановлюваний шлях у сесійній cookie. За замовчуванням `/`. Дивіться також [sessiongetcookieparams()](function.session-get-cookie-params.html) і [sessionsetcookieparams()](function.session-set-cookie-params.html)

`session.cookie_domain` string

`session.cookie_domain` визначає встановлюваний домен у сесійній cookie. Відповідно до специфікації немає сенсу додатково вказувати ім'я хоста, що згенерував cookies. Дивіться також [sessiongetcookieparams()](function.session-get-cookie-params.html) і [sessionsetcookieparams()](function.session-set-cookie-params.html)

`session.cookie_secure` bool

`session.cookie_secure` вказує, чи повинні cookie передаватися тільки через захищене з'єднання. За замовчуванням `off`. Дивіться також [sessiongetcookieparams()](function.session-get-cookie-params.html) і [sessionsetcookieparams()](function.session-set-cookie-params.html)

`session.cookie_httponly` bool

Позначка, за якою доступ до cookie з ідентифікатором сесії може бути отриманий тільки через протокол HTTP. Це означає, що cookie не буде доступною через скриптові мови, такі як JavaScript. Ця установка дозволяє ефективно захистити від XSS-атак (на жаль, ця функція підтримується не всіма браузерами).

`session.cookie_samesite` string

Дозволяє серверам стверджувати, що cookie не має надсилатися разом із міжсайтовими запитами. Це твердження дозволяє браузерам користувачів знизити ризик витоку інформації з різних джерел та забезпечує певний захист від підробки запитів. Зауважте, що це підтримується не всіма браузерами. Порожнє значення означає, що атрибут cookie сайту не буде встановлений . `Lax` і `Strict` означають, що cookie не буде надіслано для кросдоменних POST-запитів; `Lax` відправить cookie для міждоменних GET-запитів, а `Strict` не робитиме цього.

`session.cache_limiter` string

`session.cache_limiter` визначає режим кешування, який використовується для сторінок сесій. Може приймати одне з таких значень: `nocache` `private` `private_no_expire` або `public`. За замовчуванням `nocache`. Докладніше про дані значення дивіться в [sessioncachelimiter()](function.session-cache-limiter.html)

`session.cache_expire` int

`session.cache_expire` вказує час життя кешованих сторінок сесій за хвилини, це ніяк не впливає на обмежувач nocache. За замовчуванням `180`. Дивіться також [sessioncacheexpire()](function.session-cache-expire.html)

`session.use_trans_sid` bool

`session.use_trans_sid` вказує, чи використовується прозора підтримка sid чи ні. За замовчуванням `0` (Вимкнено).

> **Зауваження**: Управління сесією на основі URL має додаткові ризики безпеки порівняно з керуванням на основі cookies. Як приклад можна згадати такі ситуації, коли користувачі можуть надіслати URL, що містить ідентифікатор активної сесії, своїм друзям електронною поштою або зберегти посилання з ідентифікатором в закладках і весь час відвідувати сайт з тим самим ідентифікатором. Починаючи з PHP 7.1.0, повний шлях URL, тобто [https://php.net/](https://php.net/)обробляється "trans sid". Раніше PHP обробляв лише відносну URL-адресу. Перезапис цільового хоста задається [session.transsidhosts](session.configuration.html#ini.session.trans-sid-hosts)

`session.trans_sid_tags` string

`session.trans_sid_tags` задає теги HTML, що перезаписуються, для включення ідентифікатора сесії коли включена підтримка прозорих "sid". За замовчуванням `a=href,area=href,frame=src,input=src,form=` `form` - Спеціальних тег . `<input hidden="session_id" name="session_name">` додається у форму.

> **Зауваження**: До PHP 7.1.0 для цього використовувався [urlrewriter.tags](outcontrol.configuration.html#ini.url-rewriter.tags). З PHP 7.1.0, `fieldset` більше не рахується за спеціальний тег.

`session.trans_sid_hosts` string

`session.trans_sid_hosts` задає, які хости будуть перезаписані для включення ідентифікатора сесії, коли включено підтримку прозорих "sid". За замовчуванням `$_SERVER['HTTP_HOST']`. Декілька хостів можна вказати через кому. Не допускається вставляти прогалини між хостами. Так правильно: `php.net,wiki.php.net,bugs.php.net`

`session.sid_length` int

`session.sid_length` дозволяє вказати довжину ідентифікатора сесії. Це значення має бути в діапазоні 22-256. 32. Якщо вам потрібна сумісність, вказуйте 32, 40 і т.д. Довші ідентифікатори складніше підібрати. Рекомендується використовувати довжину щонайменше 32.

**Підказка**

Нотатки сумісності: Використовуйте 32 для `session.hash_function`0 (MD5) та `session.hash_bits_per_character` `session.hash_function`1 (SHA1) та `session.hash_bits_per_character`6\. 26 для `session.hash_function`0 (MD5) та `session.hash_bits_per_character`5\. 22 для `session.hash_function`0 (MD5) та `session.hash_bits_per_character`6\. Ви повинні налаштувати INI-налаштування таким чином, щоб ідентифікатор сесії складався як мінімум із 128 біт. Не забудьте задати відповідні значення для `session.sid_bits_per_character`інакше ваші ідентифікатори будуть слабкими.

> **Зауваження**: Ця настройка з'явилася в PHP 7.1.0

`session.sid_bits_per_character` int

`session.sid_bits_per_character` дозволяє встановити кількість біт в одному символі ідентифікатора сесії. Доступні значення '4' (0-9, a-f), '5' (0-9, a-v), і '6' (0-9, a-z, A-Z, "-", ","). 4. Чим більше біт, тим сильніший ідентифікатор сесії. У більшості оточень рекомендується 5.

> **Зауваження**: Ця настройка з'явилася в PHP 7.1.0

`session.hash_function` [mixed](language.types.declarations.html#language.types.declarations.mixed)

`session.hash_function` дозволяє вказати алгоритм хешування, що використовується для створення ідентифікатора сесії. '0' означає MD5 (128 bits), а '1' означає SHA-1 (160 bits).

Можливо вказати будь-який з алгоритмів, передбачених [модулем hash](ref.hash.md) (якщо він доступний), наприклад, `sha512` або `whirlpool`. Повний список алгоритмів можна отримати за допомогою функції [hashalgos()](function.hash-algos.html)

> **Зауваження**: Видалено в PHP 7.1.0.

`session.hash_bits_per_character` int

`session.hash_bits_per_character` дозволяє вказати скільки біт зберігається в кожному символі при перетворенні бінарного уявлення в щось більш легкочитане. Можливі значення: '4' (0-9, a-f), '5' (0-9, a-v) та '6' (0-9, a-z, A-Z, "-", ",").

> **Зауваження**: Видалено в PHP 7.1.0.

`session.upload_progress.enabled` bool

Включає відстеження прогресу завантаження файлів та заповнення відповідної змінної в масиві [SESSION](reserved.variables.session.md). За замовчуванням 1 увімкнено.

`session.upload_progress.cleanup` bool

Чистка інформації про прогрес завантаження файлів після завершення обробки POST-даних (тобто коли завантаження завершено). За замовчуванням 1 увімкнено.

> **Зауваження**: Строго рекомендується не відключати цю опцію.

`session.upload_progress.prefix` string

Префікс, який використовується для ключа прогресу завантаження в масиві [SESSION](reserved.variables.session.md). Для забезпечення унікальності цей ключ буде приєднано до значення `$_POST[ini_get("session.upload_progress.name")]`. За промовчанням дорівнює "uploadprogress".

`session.upload_progress.name` string

Ім'я ключа, що використовується в масиві [SESSION](reserved.variables.session.md)для зберігання інформації про прогрес. Дивіться також директиву [session.uploadprogress.prefix](session.configuration.html#ini.session.upload-progress.prefix). Якщо елемент `$_POST[ini_get("session.upload_progress.name")]` не передано, прогрес завантаження цього файлу не буде відстежуватися. За замовчуванням "PHPSESSIONUPLOADPROGRESS".

`session.upload_progress.freq` [mixed](language.types.declarations.html#language.types.declarations.mixed)

Визначає частоту оновлення інформації про прогрес завантаження. Можна вказати значення в байтах (тобто "оновлювати інформацію про прогрес кожні 100 байт") або у відсотках (тобто "оновлювати інформацію про прогрес після отримання 1% даних від розміру файлу"). За замовчуванням "1%".

`session.upload_progress.min_freq` int

Мінімальна затримка між оновленнями в секундах. За промовчанням "1" (одна секунда).

`session.lazy_write` bool

Якщо `session.lazy_write` встановлено в 1, то дані сесії перезаписуватимуться тільки при їх зміні. За замовчуванням 1 увімкнено.

Прогрес завантаження файлів не оброблятиметься, якщо не ввімкнено опцію session.uploadprogress.enabled і не встановлена ​​змінна $POSTiniget("session.uploadпрогрес.наме"). Докладніше про це дивіться у розділі "[Отслеживание прогресса загрузки файлов с помощью сессий](session.upload-progress.html)".