---
navigation:
  - streamwrapper.url-stat.md: '« streamWrapper::urlstat'
  - function.stream-bucket-append.md: streambucketappend »
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Функції для роботи з потоками
---
# Функції для роботи з потоками

## Зміст

-   [streambucketappend](function.stream-bucket-append.md) - Додати відро (bucket) до бригади (brigade)
-   [streambucketmakewriteable](function.stream-bucket-make-writeable.md) — Повертає об'єкт кошика із бригади для подальшої роботи з ним
-   [streambucketnew](function.stream-bucket-new.md) — Створити нове цебро для використання в поточному потоці
-   [streambucketprepend](function.stream-bucket-prepend.md) — Додати відро на початок бригади
-   [streamcontextcreate](function.stream-context-create.md) - Створює контекст потоку
-   [streamcontextgetdefault](function.stream-context-get-default.md) — Отримує контекст потоку за умовчанням
-   [streamcontextgetoptions](function.stream-context-get-options.md) — Отримує опції для потоку/обгортки/контексту
-   [streamcontextgetparams](function.stream-context-get-params.md) — Отримує параметри із контексту
-   [streamcontextsetdefault](function.stream-context-set-default.md) — Встановити контекст потоку за промовчанням
-   [streamcontextsetoption](function.stream-context-set-option.md) — Встановлює опцію для потоку/обгортки/контексту
-   [streamcontextsetparams](function.stream-context-set-params.md) — Встановлює параметри потоку/обгортки/контексту
-   [streamcopyтоstream](function.stream-copy-to-stream.md) — Копіює дані з одного потоку до іншого
-   [streamfilterappend](function.stream-filter-append.md) — Прикріпити фільтр до потоку
-   [streamfilterprepend](function.stream-filter-prepend.md) - Прикріплює фільтр до потоку
-   [streamfilterregister](function.stream-filter-register.md) — Реєструє потоковий фільтр, визначений користувачем
-   [streamfilterremove](function.stream-filter-remove.md) — Видалити фільтр із потоку
-   [streamgetcontents](function.stream-get-contents.md) — Читає частину потоку, що залишилася, в рядок
-   [streamgetfilters](function.stream-get-filters.md) — Отримати список зареєстрованих фільтрів
-   [streamgetline](function.stream-get-line.md) — Отримує рядок із потокового ресурсу до вказаного роздільника
-   [streamgetmetadata](function.stream-get-meta-data.md) — Витягує заголовок/метадані з потоків/файлових покажчиків
-   [streamgettransports](function.stream-get-transports.md) - Отримати список зареєстрованих транспортів сокету
-   [streamgetwrappers](function.stream-get-wrappers.md) — Отримати список зареєстрованих потоків
-   [streamісlocal](function.stream-is-local.md) — Перевіряє, чи потік є локальним потоком
-   [streamisatty](function.stream-isatty.md) — Перевіряє, чи є потік TTY
-   [streamnotificationcallback](function.stream-notification-callback.md) — Callback-функція параметра контексту notification
-   [streamregisterwrapper](function.stream-register-wrapper.md) - Псевдонім streamwrapperregister
-   [streamresolveincludepath](function.stream-resolve-include-path.md) — Перетворити повне ім'я файлу, використовуючи шляхи увімкнення
-   [streamselect](function.stream-select.md) — Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [streamsetblocking](function.stream-set-blocking.md) — Встановити блокуючий/неблокуючий режим у потоці
-   [streamsetchunksize](function.stream-set-chunk-size.md) — Встановити розмір фрагмента даних потоку
-   [streamsetreadbuffer](function.stream-set-read-buffer.md) — Встановити буферизацію читання файлу на вказаному потоці
-   [streamsettimeout](function.stream-set-timeout.md) — Встановити час очікування для потоку
-   [streamsetwritebuffer](function.stream-set-write-buffer.md) — Встановлює буферизацію файлу під час запису у вказаний потік
-   [streamsocketaccept](function.stream-socket-accept.md) — Приймати з'єднання в сокеті, створеному за допомогою функції streamsocketserver
-   [streamsocketclient](function.stream-socket-client.md) — Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [streamsocketenablecrypto](function.stream-socket-enable-crypto.md) — Вмикає або вимикає шифрування на вже підключеному сокеті
-   [streamsocketgetname](function.stream-socket-get-name.md) — Отримати назву локального чи віддаленого сокету
-   [streamsocketpair](function.stream-socket-pair.md) — Створює пару підключених, невиразних потоків сокетів
-   [streamsocketrecvfrom](function.stream-socket-recvfrom.md) — Отримує дані із сокету, підключеного чи ні
-   [streamsocketsendto](function.stream-socket-sendto.md) — Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні
-   [streamsocketserver](function.stream-socket-server.md) - Створює інтернет-сокет або доменний сокет Unix
-   [streamsocketshutdown](function.stream-socket-shutdown.md) — Закрити повнодуплексне з'єднання
-   [streamsupportslock](function.stream-supports-lock.md) — Визначає, чи потік підтримує блокування
-   [streamwrapperregister](function.stream-wrapper-register.md) - Реєструє обгортку URL, реалізовану у вигляді PHP-класу
-   [streamwrapperrestore](function.stream-wrapper-restore.md) — Відновлює скасовану раніше вбудовану обгортку
-   [streamwrapperunregister](function.stream-wrapper-unregister.md) — Скасує реєстрацію обгортки URL
