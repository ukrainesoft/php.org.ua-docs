Функції для роботи з потоками

-   [« streamWrapper::urlstat](streamwrapper.url-stat.html)
    
-   [streambucketappend »](function.stream-bucket-append.html)
    
-   [PHP Manual](index.md)
    
-   [Потоки](book.stream.md)
    
-   Функції для роботи з потоками
    

# Функції для роботи з потоками

## Зміст

-   [streambucketappend](function.stream-bucket-append.html) - Додати відро (bucket) до бригади (brigade)
-   [streambucketmakewriteable](function.stream-bucket-make-writeable.html) — Повертає об'єкт кошика із бригади для подальшої роботи з ним
-   [streambucketnew](function.stream-bucket-new.html) — Створити нове цебро для використання в поточному потоці
-   [streambucketprepend](function.stream-bucket-prepend.html) — Додати відро на початок бригади
-   [streamcontextcreate](function.stream-context-create.html) - Створює контекст потоку
-   [streamcontextgetdefault](function.stream-context-get-default.html) — Отримує контекст потоку за умовчанням
-   [streamcontextgetoptions](function.stream-context-get-options.html) — Отримує опції для потоку/обгортки/контексту
-   [streamcontextgetparams](function.stream-context-get-params.html) — Отримує параметри із контексту
-   [streamcontextsetdefault](function.stream-context-set-default.html) — Встановити контекст потоку за промовчанням
-   [streamcontextsetoption](function.stream-context-set-option.html) — Встановлює опцію для потоку/обгортки/контексту
-   [streamcontextsetparams](function.stream-context-set-params.html) — Встановлює параметри потоку/обгортки/контексту
-   [streamcopyтоstream](function.stream-copy-to-stream.html) — Копіює дані з одного потоку до іншого
-   [streamfilterappend](function.stream-filter-append.html) — Прикріпити фільтр до потоку
-   [streamfilterprepend](function.stream-filter-prepend.html) - Прикріплює фільтр до потоку
-   [streamfilterregister](function.stream-filter-register.html) — Реєструє потоковий фільтр, визначений користувачем
-   [streamfilterremove](function.stream-filter-remove.html) — Видалити фільтр із потоку
-   [streamgetcontents](function.stream-get-contents.html) — Читає частину потоку, що залишилася, в рядок
-   [streamgetfilters](function.stream-get-filters.html) — Отримати список зареєстрованих фільтрів
-   [streamgetline](function.stream-get-line.html) — Отримує рядок із потокового ресурсу до вказаного роздільника
-   [streamgetmetadata](function.stream-get-meta-data.html) — Витягує заголовок/метадані з потоків/файлових покажчиків
-   [streamgettransports](function.stream-get-transports.html) - Отримати список зареєстрованих транспортів сокету
-   [streamgetwrappers](function.stream-get-wrappers.html) — Отримати список зареєстрованих потоків
-   [streamісlocal](function.stream-is-local.html) — Перевіряє, чи потік є локальним потоком
-   [streamisatty](function.stream-isatty.html) — Перевіряє, чи є потік TTY
-   [streamnotificationcallback](function.stream-notification-callback.html) — Callback-функція параметра контексту notification
-   [streamregisterwrapper](function.stream-register-wrapper.html) - Псевдонім streamwrapperregister
-   [streamresolveincludepath](function.stream-resolve-include-path.html) — Перетворити повне ім'я файлу, використовуючи шляхи увімкнення
-   [streamselect](function.stream-select.html) — Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [streamsetblocking](function.stream-set-blocking.html) — Встановити блокуючий/неблокуючий режим у потоці
-   [streamsetchunksize](function.stream-set-chunk-size.html) — Встановити розмір фрагмента даних потоку
-   [streamsetreadbuffer](function.stream-set-read-buffer.html) — Встановити буферизацію читання файлу на вказаному потоці
-   [streamsettimeout](function.stream-set-timeout.html) — Встановити час очікування для потоку
-   [streamsetwritebuffer](function.stream-set-write-buffer.html) — Встановлює буферизацію файлу під час запису у вказаний потік
-   [streamsocketaccept](function.stream-socket-accept.html) — Приймати з'єднання в сокеті, створеному за допомогою функції streamsocketserver
-   [streamsocketclient](function.stream-socket-client.html) — Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [streamsocketenablecrypto](function.stream-socket-enable-crypto.html) — Вмикає або вимикає шифрування на вже підключеному сокеті
-   [streamsocketgetname](function.stream-socket-get-name.html) — Отримати назву локального чи віддаленого сокету
-   [streamsocketpair](function.stream-socket-pair.html) — Створює пару підключених, невиразних потоків сокетів
-   [streamsocketrecvfrom](function.stream-socket-recvfrom.html) — Отримує дані із сокету, підключеного чи ні
-   [streamsocketsendto](function.stream-socket-sendto.html) — Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні
-   [streamsocketserver](function.stream-socket-server.html) - Створює інтернет-сокет або доменний сокет Unix
-   [streamsocketshutdown](function.stream-socket-shutdown.html) — Закрити повнодуплексне з'єднання
-   [streamsupportslock](function.stream-supports-lock.html) — Визначає, чи потік підтримує блокування
-   [streamwrapperregister](function.stream-wrapper-register.html) - Реєструє обгортку URL, реалізовану у вигляді PHP-класу
-   [streamwrapperrestore](function.stream-wrapper-restore.html) — Відновлює скасовану раніше вбудовану обгортку
-   [streamwrapperunregister](function.stream-wrapper-unregister.html) — Скасує реєстрацію обгортки URL