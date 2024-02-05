---
navigation:
  - session.installation.md: « Встановлення
  - session.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - session.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування механізму сесій**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [session.save\_path](session.configuration.md#ini.session.save-path) | "" | **`INI_ALL`** |  |
| [session.name](session.configuration.md#ini.session.name) | "PHPSESSID" | **`INI_ALL`** |  |
| [session.save\_handler](session.configuration.md#ini.session.save-handler) | "files" | **`INI_ALL`** |  |
| [session.auto\_start](session.configuration.md#ini.session.auto-start) | "0" | **`INI_PERDIR`** |  |
| [session.gc\_probability](session.configuration.md#ini.session.gc-probability) | "1" | **`INI_ALL`** |  |
| [session.gc\_divisor](session.configuration.md#ini.session.gc-divisor) | "100" | **`INI_ALL`** |  |
| [session.gc\_maxlifetime](session.configuration.md#ini.session.gc-maxlifetime) | "1440" | **`INI_ALL`** |  |
| [session.serialize\_handler](session.configuration.md#ini.session.serialize-handler) | "php" | **`INI_ALL`** |  |
| [session.cookie\_lifetime](session.configuration.md#ini.session.cookie-lifetime) | "0" | **`INI_ALL`** |  |
| [session.cookie\_path](session.configuration.md#ini.session.cookie-path) | "/" | **`INI_ALL`** |  |
| [session.cookie\_domain](session.configuration.md#ini.session.cookie-domain) | "" | **`INI_ALL`** |  |
| [session.cookie\_secure](session.configuration.md#ini.session.cookie-secure) | "0" | **`INI_ALL`** | До PHP 7.2.0 значення за промовчанням було `""` |
| [session.cookie\_httponly](session.configuration.md#ini.session.cookie-httponly) | "0" | **`INI_ALL`** | До PHP 7.2.0 значення за промовчанням було `""` |
| [session.cookie\_samesite](session.configuration.md#ini.session.cookie-samesite) | "" | **`INI_ALL`** | Доступна з PHP 7.3.0. |
| [session.use\_strict\_mode](session.configuration.md#ini.session.use-strict-mode) | "0" | **`INI_ALL`** |  |
| [session.use\_cookies](session.configuration.md#ini.session.use-cookies) | "1" | **`INI_ALL`** |  |
| [session.use\_only\_cookies](session.configuration.md#ini.session.use-only-cookies) | "1" | **`INI_ALL`** |  |
| [session.referer\_check](session.configuration.md#ini.session.referer-check) | "" | **`INI_ALL`** |  |
| [session.cache\_limiter](session.configuration.md#ini.session.cache-limiter) | "nocache" | **`INI_ALL`** |  |
| [session.cache\_expire](session.configuration.md#ini.session.cache-expire) | "180" | **`INI_ALL`** |  |
| [session.use\_trans\_sid](session.configuration.md#ini.session.use-trans-sid) | "0" | **`INI_ALL`** |  |
| [session.trans\_sid\_tags](session.configuration.md#ini.session.trans-sid-tags) | "a=href,area=href,frame=src,form=" | **`INI_ALL`** | Доступна з PHP 7.1.0. |
| [session.trans\_sid\_hosts](session.configuration.md#ini.session.trans-sid-hosts) | `$_SERVER['HTTP_HOST']` | **`INI_ALL`** | Доступна з PHP 7.1.0. |
| [session.sid\_length](session.configuration.md#ini.session.sid-length) | "32" | **`INI_ALL`** | Доступна з PHP 7.1.0. |
| [session.sid\_bits\_per\_character](session.configuration.md#ini.session.sid-bits-per-character) | "4" | **`INI_ALL`** | Доступна з PHP 7.1.0. |
| [session.upload\_progress.enabled](session.configuration.md#ini.session.upload-progress.enabled) | "1" | **`INI_PERDIR`** |  |
| [session.upload\_progress.cleanup](session.configuration.md#ini.session.upload-progress.cleanup) | "1" | **`INI_PERDIR`** |  |
| [session.upload\_progress.prefix](session.configuration.md#ini.session.upload-progress.prefix) | "upload\_progress\_" | **`INI_PERDIR`** |  |
| [session.upload\_progress.name](session.configuration.md#ini.session.upload-progress.name) | "PHP\_SESSION\_UPLOAD\_PROGRESS" | **`INI_PERDIR`** |  |
| [session.upload\_progress.freq](session.configuration.md#ini.session.upload-progress.freq) | "1%" | **`INI_PERDIR`** |  |
| [session.upload\_progress.min\_freq](session.configuration.md#ini.session.upload-progress.min-freq) | "1" | **`INI_PERDIR`** |  |
| [session.lazy\_write](session.configuration.md#ini.session.lazy-write) | "1" | **`INI_ALL`** |  |
| [session.hash\_function](session.configuration.md#ini.session.hash-function) | "0" | **`INI_ALL`** | Видалено в PHP 7.1.0. |
| [session.hash\_bits\_per\_character](session.configuration.md#ini.session.hash-bits-per-character) | "4" | **`INI_ALL`** | Видалено в PHP 7.1.0. |
| [session.entropy\_file](session.configuration.md#ini.session.entropy-file) | "" | **`INI_ALL`** | Видалено в PHP 7.1.0. |
| [session.entropy\_length](session.configuration.md#ini.session.entropy-length) | "0" | **`INI_ALL`** | Видалено в PHP 7.1.0 |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Система керування сесіями підтримує низку опцій, які можуть бути вказані у файлі php.ini. Нижче наведено короткий огляд.

`session.save_handler`string

`session.save_handler` визначає ім'я оброблювача, який використовується для зберігання та вилучення даних, пов'язаних із сесією. За замовчуванням має значення `files`. Слід звернути увагу на те, що деякі модулі можуть зареєструвати власні обробники (`save_handler`). Поточні зареєстровані обробники відображаються в [phpinfo()](function.phpinfo.md)Смотрите также[session\_set\_save\_handler()](function.session-set-save-handler.md)

`session.save_path`string

`session.save_path` визначає аргумент, який передається до обробника збереження. Якщо вибраний обробник файлів за промовчанням, аргумент містить шлях, яким створюватимуться файли. Дивіться також опис функції [session\_save\_path()](function.session-save-path.md)

Для цієї директиви можна поставити необов'язковий аргумент `N`, Який визначає глибину вкладених директорій, якими будуть розподілені файли сесій. Наприклад, встановлення значення `'5;/tmp'` може розташувати створений файл сесії таким шляхом: `/tmp/4/b/1/e/3/sess_4b1e384ad74619bd212e236e52a5a174If`. Щоб використати аргумент `N`Спочатку необхідно створити всі ці директорії. Для цього в директорії ext/session існує невеликий скрипт оболонки, який у Linux-системах називається mod\_files.sh, а в системах Windows mod\_files.bat. Зауважте також, що якщо аргумент `N` визначено і більше 0, то автоматичне складання сміття не виконується, докладніше про це написано у файлі php.ini. А також якщо заданий аргумент `N`необхідно переконатися, що значення директиви `session.save_path` вказано в лапках, оскільки роздільник ( ) у файлі php.ini також вказують для коментарів.

Модуль зберігання файлів створює файли з правами 600 за промовчанням. Значення за умовчанням можна змінити необов'язковим аргументом `MODE` `N;MODE;/path`, где`MODE`— восьмеричное представление режима доступа к файлу. Установка аргумента`MODE`не влияет на обработку umask.

**Увага**

Якщо встановити як загальнодоступну для читання директорію, наприклад, /tmp (за замовчуванням), решта користувачів сервера зможуть перехопити сесію користувача, отримавши список файлів у цій директорії.

**Застереження**

При зазначенні вже описаного необов'язкового аргументу рівня вкладеності директорій `N`, враховують, що значення вище 1 або 2 неприпустимо для більшої частини сайтів через те, що потрібно створити багато директорій: наприклад, значення 3 означає, що у файловій системі існує `(2 ** session.sid_bits_per_character) ** 3` директорій, які можуть даремно займати багато дискового простору та індексних дескрипторів (inodes).

Значения больше 2 для аргумента`N` вказують, тільки якщо абсолютно впевнені, що розмір сайту відповідає такій вимогі.

`session.name`string

`session.name` визначає назву сесії, яка буде використана як назва cookies. Може містити лише цифри та літери. За замовчуванням одно `PHPSESSID`Смотрите также описание функции[session\_name()](function.session-name.md)

`session.auto_start`bool

`session.auto_start` визначає, чи модуль сесії запускатиме сесію автоматично при старті. Значення за замовчуванням (отключено).

`session.serialize_handler`string

`session.serialize_handler` визначає ім'я оброблювача, який буде використаний для серіалізації/десеріалізації даних. Підтримується формат серіалізації PHP (найменування `php_serialize`), внутренний формат PHP (наименование`php`и`php_binary`) та WDDX (найменування `wddx`). WDDX доступний тільки в тому випадку, якщо PHP скомпільовано з [підтримкою WDDX](ref.wddx.md). . `php_serialize` використовує просту функцію серіалізації/десеріалізації для внутрішніх потреб і не має тих обмежень, які є у `php`и`php_binary`. Старі обробники серіалізації не можуть зберігати ні числові, ні рядкові індекси, що містять спеціальні символи ( и`!`) у $\_SESSION. Используйте`php_serialize`, щоб уникнути помилок числових і рядкових індексів при завершенні скрипту. Значення за замовчуванням `php`

`session.gc_probability`int

`session.gc_probability` в поєднанні з `session.gc_divisor` визначає ймовірність запуску функції збирача сміття (gc, garbage collection). За замовчуванням дорівнює Смотрите подробнее в[session.gc\_divisor](session.configuration.md#ini.session.gc-divisor)

`session.gc_divisor`int

`session.gc_divisor` в поєднанні з `session.gc_probability` визначає можливість запуску функції збирача сміття (gc, garbage collection) при кожній ініціалізації сесії. Імовірність розраховується як gc\_probability/gc\_divisor, тобто 1/100 означає, що функція gc запускається в одному випадку зі ста, або 1% при кожному запиті . `session.gc_divisor`по умолчанию имеет значение

`session.gc_maxlifetime`int

`session.gc_maxlifetime` задає відстрочку часу в секундах, після якої дані будуть розглядатися як "сміття" та потенційно будуть видалені. Збір сміття може відбутися протягом старту сесії (залежно від значень [session.gc\_probability](session.configuration.md#ini.session.gc-probability) і [session.gc\_divisor](session.configuration.md#ini.session.gc-divisor)). По умолчанию значение`1440` (24 хвилини).

> **Зауваження**: Якщо різні скрипти мають різні значення `session.gc_maxlifetime`Але при цьому одні й ті ж місця для зберігання даних сесії, то скрипт з мінімальним значенням знищить усі дані. У такому разі слід використовувати цю директиву разом з [session.save\_path](session.configuration.md#ini.session.save-path)

`session.referer_check`string

`session.referer_check` містить підрядок, який можна використовувати під час перевірки HTTP Referer. Якщо клієнтом був надісланий referer і підрядок не був виявлений, то ідентифікатор сесії буде позначений як недійсний. За промовчанням використовується порожній рядок.

`session.entropy_file`string

`session.entropy_file` містить шлях до ресурсу (файлу), що використовується як додаткове джерело ентропії у процесі створення ідентифікатора сесії. Наприклад, `/dev/random`или`/dev/urandom`, які доступні на багатьох Unix-системах. Ця можливість також підтримується у Windows. Вказівка ​​ненульового значення в `session.entropy_length` наказує PHP використовувати як джерело ентропії Windows Random API.

> **Зауваження**: Удалено в PHP 7.1.0`session.entropy_file`имеет значение по умолчанию равное`/dev/urandom`или`/dev/arandom`якщо вони доступні.

`session.entropy_length`int

`session.entropy_length` визначає кількість байт, які будуть прочитані з вказаного вище файлу. За замовчуванням `32`Удалено в PHP 7.1.0.

`session.use_strict_mode`bool

`session.use_strict_mode` визначає, чи буде модуль використовувати режим суворого ідентифікатора (ID). Якщо від браузера отримано невизначений ID, браузеру буде надіслано новий ID. Таким чином, програми захищаються від фіксації сесії за допомогою суворого режиму. За замовчуванням (отключено).

> **Зауваження**: Включение`session.use_strict_mode` є обов'язковим для спільної безпеки сесії. Всім сайтам рекомендується її вмикати. Дивіться приклади [session\_create\_id()](function.session-create-id.md)

**Увага**

Якщо користувальницький обробник сесії, зареєстрований за допомогою [session\_set\_save\_handler()](function.session-set-save-handler.md), не реалізує [SessionUpdateTimestampHandlerInterface::validateId()](sessionupdatetimestamphandlerinterface.validateid.md)и не предоставляет callback-функцию`validate_sid`відповідно, режим суворого ідентифікатора сесії буде відключений, незалежно від значення цієї директиви. Особливо зверніть увагу, що [SessionHandler](class.sessionhandler.md) *не* реалізує **SessionHandler::validateId()**

`session.use_cookies`bool

`session.use_cookies` визначає, чи модуль використовуватиме cookies для зберігання ідентифікатора сесії на стороні клієнта. За замовчуванням (включено).

`session.use_only_cookies`bool

`session.use_only_cookies` визначає, чи модуль використовуватиме **тільки** cookies для зберігання сесії ідентифікатора на стороні клієнта. Увімкнення цього параметра запобігає атакам з використанням ідентифікатора сесії, розміщеного в URL. Значення за замовчуванням (включено).

`session.cookie_lifetime`int

`session.cookie_lifetime` вказує час життя cookies, що надсилається до браузера клієнта, в секундах. Значення 0 означає, що cookies будуть валідними до закриття браузера. За замовчуванням одно Смотрите также[session\_get\_cookie\_params()](function.session-get-cookie-params.md) і [session\_set\_cookie\_params()](function.session-set-cookie-params.md)

> **Зауваження**: Позначка закінчення часу встановлюється по відношенню до серверного часу, який не обов'язково збігається з часом у браузері клієнта.

`session.cookie_path`string

`session.cookie_path` визначає встановлюваний шлях у сесійній cookie. За замовчуванням Смотрите также[session\_get\_cookie\_params()](function.session-get-cookie-params.md) і [session\_set\_cookie\_params()](function.session-set-cookie-params.md)

`session.cookie_domain`string

`session.cookie_domain` визначає встановлюваний домен у сесійній cookie. Відповідно до специфікації немає сенсу додатково вказувати ім'я хоста, що згенерував cookies. Дивіться також [session\_get\_cookie\_params()](function.session-get-cookie-params.md) і [session\_set\_cookie\_params()](function.session-set-cookie-params.md)

`session.cookie_secure`bool

`session.cookie_secure` вказує, чи повинні cookie передаватися тільки через захищене з'єднання. Коли для цього налаштування встановлено значення `on`, сесії працюють лише з HTTPS-з'єднаннями. Якщо значення `off`, Сесії працюють і з HTTP-, і з HTTPS-з'єднаннями. Значення за замовчуванням `off`Смотрите также описание функций[session\_get\_cookie\_params()](function.session-get-cookie-params.md) і [session\_set\_cookie\_params()](function.session-set-cookie-params.md)

`session.cookie_httponly`bool

Позначка, за якою доступ до cookie з ідентифікатором сесії може бути отриманий тільки через протокол HTTP. Це означає, що cookie не буде доступна через скриптові мови, такі як JavaScript. Ця установка дозволяє ефективно захистити від XSS-атак (на жаль, ця функція підтримується не всіма браузерами).

`session.cookie_samesite`string

Дозволяє серверам стверджувати, що cookie не має надсилатися разом із міжсайтовими запитами. Це твердження дозволяє браузерам користувачів знизити ризик витоку інформації з різних джерел та забезпечує певний захист від підробки запитів. Зауважте, що це підтримується не всіма браузерами. Порожнє значення означає, що атрибут cookie сайту не буде встановлений . `Lax`и`Strict` означають, що cookie не буде надіслано для кросдоменних POST-запитів; `Lax` відправить cookie для міждоменних GET-запитів, а `Strict` не робитиме цього.

`session.cache_limiter`string

`session.cache_limiter` визначає режим кешування, який використовується для сторінок сесій. Може приймати одне з таких значень: `nocache` `private` `private_no_expire`или`public`По умолчанию`nocache`. Детальніше про дані значення дивіться в [session\_cache\_limiter()](function.session-cache-limiter.md)

`session.cache_expire`int

`session.cache_expire` вказує час життя кешованих сторінок сесій за хвилини, це ніяк не впливає на обмежувач nocache. За замовчуванням `180`Смотрите также[session\_cache\_expire()](function.session-cache-expire.md)

`session.use_trans_sid`bool

`session.use_trans_sid` вказує, чи використовується прозора підтримка sid чи ні. За замовчуванням (отключено).

> **Зауваження**: Управління сесією на основі URL має додаткові ризики безпеки порівняно з керуванням на основі cookies. Як приклад можна згадати такі ситуації, коли користувачі можуть надіслати URL, що містить ідентифікатор активної сесії, своїм друзям електронною поштою або зберегти посилання з ідентифікатором в закладках і весь час відвідувати сайт з тим самим ідентифікатором. Починаючи з PHP 7.1.0, повний шлях URL, тобто [https://php.net/](https://php.net/)обробляється "trans sid". Раніше PHP обробляв лише відносну URL-адресу. Перезапис цільового хоста задається [session.trans\_sid\_hosts](session.configuration.md#ini.session.trans-sid-hosts)

`session.trans_sid_tags`string

`session.trans_sid_tags` задає теги HTML, що перезаписуються, для включення ідентифікатора сесії коли включена підтримка прозорих "sid". За замовчуванням `a=href,area=href,frame=src,input=src,form=` `form` - Спеціальних тег . `<input hidden="session_id" name="session_name">`добавляется в форму.

> **Зауваження**: До PHP 7.1.0 для цього використовувався [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags)С PHP 7.1.0,`fieldset` більше не рахується за спеціальний тег.

`session.trans_sid_hosts`string

`session.trans_sid_hosts` задає, які хости будуть перезаписані для включення ідентифікатора сесії, коли включено підтримку прозорих "sid". За замовчуванням `$_SERVER['HTTP_HOST']`. Декілька хостів можна вказати через кому. Не допускається вставляти прогалини між хостами. Так правильно: `php.net,wiki.php.net,bugs.php.net`

`session.sid_length`int

`session.sid_length` дозволяє вказати довжину ідентифікатора сесії. Це значення має бути в діапазоні 22-256. За замовчуванням 32. Якщо вам потрібна сумісність, вказуйте 32, 40 і т.д. Довші ідентифікатори складніше підібрати. Рекомендується використовувати довжину щонайменше 32.

**Підказка**

Заметки по совместимости: Используйте 32 для`session.hash_function`\=0 (MD5) и`session.hash_bits_per_character`\= `session.hash_function`\=1 (SHA1) и`session.hash_bits_per_character`\=6. 26 для`session.hash_function`\=0 (MD5) и`session.hash_bits_per_character`\=5. 22 для`session.hash_function`\=0 (MD5) и`session.hash_bits_per_character`\=6. Ви повинні налаштувати INI-налаштування таким чином, щоб ідентифікатор сесії складався як мінімум зі 128 біт. Не забудьте задати відповідні значення для `session.sid_bits_per_character`інакше ваші ідентифікатори будуть слабкими.

> **Зауваження**: Ця настройка з'явилася в PHP 7.1.0

`session.sid_bits_per_character`int

`session.sid_bits_per_character` дозволяє встановити кількість біт в одному символі ідентифікатора сесії. Доступні значення '4' (0-9, a-f), '5' (0-9, a-v), і '6' (0-9, a-z, A-Z, "-", ","). 4. Чим більше біт, тим сильніший ідентифікатор сесії. У більшості оточень рекомендується 5.

> **Зауваження**: Ця настройка з'явилася в PHP 7.1.0

`session.hash_function` [mixed](language.types.declarations.md#language.types.declarations.mixed)

`session.hash_function` дозволяє вказати алгоритм хешування, що використовується для створення ідентифікатора сесії. '0' означає MD5 (128 bits), а '1' означає SHA-1 (160 bits).

Можливо вказати будь-який з алгоритмів, передбачених [модулем hash](ref.hash.md)(если он доступен), наПриклад,`sha512`или`whirlpool`. Повний список алгоритмів можна отримати за допомогою функції [hash\_algos()](function.hash-algos.md)

> **Зауваження**: Видалено в PHP 7.1.0.

`session.hash_bits_per_character`int

`session.hash_bits_per_character` дозволяє вказати скільки біт зберігається в кожному символі при перетворенні бінарного уявлення в щось більш легкочитане. Можливі значення: '4' (0-9, a-f), '5' (0-9, a-v) та '6' (0-9, a-z, A-Z, "-", ",").

> **Зауваження**: Видалено в PHP 7.1.0.

`session.upload_progress.enabled`bool

Включає відстеження прогресу завантаження файлів та заповнення відповідної змінної в масиві [$\_SESSION](reserved.variables.session.md)По умолчанию 1, включено.

`session.upload_progress.cleanup`bool

Чистка інформації про прогрес завантаження файлів після завершення обробки POST-даних (тобто коли завантаження завершено). За замовчуванням 1 увімкнено.

> **Зауваження**: Строго рекомендується не відключати цю опцію.

`session.upload_progress.prefix`string

Префікс, який використовується для ключа прогресу завантаження в масиві [$\_SESSION](reserved.variables.session.md). Для забезпечення унікальності цей ключ буде приєднано до значення `$_POST[ini_get("session.upload_progress.name")]`. . За промовчанням дорівнює "upload\_progress\_".

`session.upload_progress.name`string

Ім'я ключа, що використовується в масиві [$\_SESSION](reserved.variables.session.md), для хранения информации о прогрессе. Смотрите также директиву[session.upload\_progress.prefix](session.configuration.md#ini.session.upload-progress.prefix). Якщо елемент `$_POST[ini_get("session.upload_progress.name")]` не передано, прогрес завантаження цього файлу не буде відстежуватися. За замовчуванням "PHP\_SESSION\_UPLOAD\_PROGRESS".

`session.upload_progress.freq` [mixed](language.types.declarations.md#language.types.declarations.mixed)

Визначає частоту оновлення інформації про прогрес завантаження. Можна вказати значення в байтах (тобто "оновлювати інформацію про прогрес кожні 100 байт") або у відсотках (тобто "оновлювати інформацію про прогрес після отримання 1% даних від розміру файлу"). За замовчуванням "1%".

`session.upload_progress.min_freq`int

Мінімальна затримка між оновленнями в секундах. За промовчанням "1" (одна секунда).

`session.lazy_write`bool

Якщо `session.lazy_write` встановлено в 1, то дані сесії перезаписуватимуться тільки при їх зміні. За замовчуванням 1 увімкнено.

Прогрес завантаження файлів не оброблятиметься, якщо не ввімкнено опцію session.upload\_progress.enabled і не встановлена ​​змінна $\_POST\[ini\_get("session.upload\_progress.name")\]. . Докладніше про це дивіться у розділі "[Відстеження прогресу завантаження файлів за допомогою сесій](session.upload-progress.md)".
