---
navigation:
  - mysqlnd.install.html: « Установка
  - mysqlnd.incompatibilities.html: Несумісності »
  - index.html: PHP Manual
  - book.mysqlnd.html: Mysqlnd
title: Налаштування під час виконання
---
# Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації вбудованого драйвера MySQL**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mysqlnd.collectstatistics](mysqlnd.config.html#ini.mysqlnd.collect-statistics) | "1" | PHPINISYSTEM |  |
| [mysqlnd.collectmemorystatistics](mysqlnd.config.html#ini.mysqlnd.collect-memory-statistics) | "0" | PHPINISYSTEM |  |
| [mysqlnd.debug](mysqlnd.config.html#ini.mysqlnd.debug) | "" | PHPINISYSTEM |  |
| [mysqlnd.logmask](mysqlnd.config.html#ini.mysqlnd.log-mask) |  | PHPINIALL |  |
| [mysqlnd.mempooldefaultsize](mysqlnd.config.html#ini.mysqlnd.mempool-default-size) |  | PHPINIALL |  |
| [mysqlnd.netreadtimeout](mysqlnd.config.html#ini.mysqlnd.net-read-timeout) | "86400" | PHPINIALL | До PHP 7.2.0 значенням за промовчанням "31536000", а місцем зміни було **`PHP_INI_SYSTEM`** |
| [mysqlnd.netcmdbuffersize](mysqlnd.config.html#ini.mysqlnd.net-cmd-buffer-size) | 5.3.0 - "2048"; 5.3.1 - "4096" | PHPINISYSTEM |  |
| [mysqlnd.netreadbuffersize](mysqlnd.config.html#ini.mysqlnd.net-read-buffer-size) | "32768" | PHPINISYSTEM |  |
| [mysqlnd.sha256serverpublickey](mysqlnd.config.html#ini.mysqlnd.sha256-server-public-key) | "" | PHPINIPERDIR |  |
| [mysqlnd.tracealloc](mysqlnd.config.html#ini.mysqlnd.trace-alloc) | "" | PHPINISYSTEM |  |
| [mysqlnd.fetchdatacopy](mysqlnd.config.html#ini.mysqlnd.fetch_data_copy) |  | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`mysqlnd.collect_statistics` bool

Включає в себе збір різної статистики клієнта, доступ до якої можна отримати за допомогою [mysqligetclientstats()](function.mysqli-get-client-stats.html) [mysqligetconnectionstats()](mysqli.get-connection-stats.html), і яка відображається у розділі `mysqlnd` виведення функції [phpinfo()](function.phpinfo.html)

Цей параметр конфігурації включає всю [статистику вбудованого драйвера MySQL](mysqlnd.stats.html), Окрім роботи з оперативною пам'яттю.

`mysqlnd.collect_memory_statistics` bool

Включає збирання різної статистики оперативної пам'яті, доступ до якої можна отримати за допомогою [mysqligetclientstats()](function.mysqli-get-client-stats.html) [mysqligetconnectionstats()](mysqli.get-connection-stats.html), і яка відображається у розділі `mysqlnd` виведення функції [phpinfo()](function.phpinfo.html)

Цей параметр конфігурації включає всю статистику, що стосується роботи з оперативною пам'яттю, в загальний набір даних [статистики вбудованого драйвера MySQL](mysqlnd.stats.html)

`mysqlnd.debug` string

Записує команди з усіх модулів, які використовують `mysqlnd`у зазначений файл з логами.

Формат параметра наступний: `mysqlnd.debug = "option1[,parameter_option1][:option2[,parameter_option2]]"`

Можливі нижченаведені значення для рядка форматування:

-   А,file - Додає виведення трасування у вказаний файл. Також щоразу перевіряє успішність запису даних. Це реалізовано шляхом закриття та повторного відкриття файлу (що досить повільно). Надає гарантію цілісності файлу з логами у разі помилки програми.
    
-   а,file - Додає виведення трасування у вказаний файл.
    
-   d - Включає виведення з макросу DBUG поточного стану. Може бути доповнено списком ключових слів, щоб вибрати висновок макросу DBUG, що містить ці ключові слова. Порожній список ключових слів передбачає виведення всіх макросів.
    
-   ф,функції - обмежує дії налагоджувача зазначеним списком функцій. Порожній список функцій передбачає вибір усіх функцій.
    
-   F - позначає виведення кожного рядка відладчика назвою вихідного файлу, що містить код, що спричинив висновок.
    
-   i - позначає виведення кожного рядка відладчика PID поточного процесу.
    
-   L - позначає виведення кожного рядка відладчика назвою вихідного файлу, що викликав висновок, і номером рядка у ній.
    
-   n - позначає виведення кожного рядка відладчика рівнем вкладеності поточної функції.
    
-   о,file - подібно до a,fileале перезаписує старий файл, а не дописує його.
    
-   Про,file - подібно до A,file але перезаписує старий файл, а чи не дописує його.
    
-   т,Н - Включає контроль функцій під час трасування. Максимальний рівень вкладеності визначено N і за умовчанням дорівнює 200.
    
-   x – цей параметр активує профільування.
    
-   m - відстежувати дзвінки, пов'язані з виділеннями та вивільненням пам'яті.
    

Приклад:

```
d:t:x:O,/tmp/mysqlnd.trace
```

> **Зауваження**
> 
> Ця можливість доступна тільки для налагодження PHP. Працює на Microsoft Windows при використанні налагоджувального складання PHP, якщо PHP було зібрано за допомогою Microsoft Visual C версії 9 і вище.

`mysqlnd.log_mask` int

Визначає, які запити журналюватимуться. Значення за промовчанням - 0, що вимикає журнал. Значення параметра – лише ціле число, константи PHP використовувати не можна. Наприклад, при значенні 48 (16 + 32) в журнал записуватимуться повільні запити, які використовують невідповідні індекси (SERVERQUERYАЛЕGOODINDEXUSED ​​= 16), або не використовують їх взагалі SERVERQUERYАЛЕINDEXUSED ​​= 32). При значенні 2043 (1 + 2 + 8 + ... + 1024) до журналу записуватимуться всі типи повільних запитів.

Використовуються такі типи запитів: SERVERSTATUSІНTRANS=1, SERVERSTATUSAUTOCOMMIT=2, SERVERMORERESULTSEXISTS=8, SERVERQUERYАЛЕGOODINDEXUSED=16, SERVERQUERYАЛЕINDEXUSED=32, SERVERSTATUSCURSOREXISTS=64, SERVERSTATUSLASTROWSENT=128, SERVERSTATUSДБDROPPED=256, SERVERSTATUSАЛЕBACKSLASHESCAPES=512, і SERVERQUERYWASSLOW = 1024.

`mysqlnd.mempool_default_size` int

Більшість розміру mysqlnd пам'яті, які використовують за результатами набору.

`mysqlnd.net_read_timeout` int

`mysqlnd` та клієнтська бібліотека MySQL, `libmysqlclient`, використовують різні мережеві API . `mysqlnd` використовує потоки PHP, тоді як `libmysqlclient` - Власну обгортку над мережевими викликами операційної системи. У PHP за промовчанням виставлено 60-секундний час очікування потоків. Цей параметр виставляється у php.ini директивою `default_socket_timeout`. За умовчанням це стосується всіх потоків, яким не встановлено інше значення часу очікування . `mysqlnd` не встановлював інших значень, тому підключення тривалих запитів можуть бути відключені після `default_socket_timeout` секунд з помилкою 2006 – MySQL Server has gone away. Клієнтська бібліотека MySQL встановлює час очікування за промовчанням 24 3600 секунд (1 день) і чекає на виникнення іншого часу очікування, такого як час очікування TCP/IP. Тепер `mysqlnd` використовує такий самий дуже довгий час очікування. Це значення можна змінити через нову директиву php.ini - `mysqlnd.net_read_timeout`. . `mysqlnd.net_read_timeout` буде використовуватися будь-яким модулем (`ext/mysql` `ext/mysqli` `PDO_MySQL`), що використовує `mysqlnd`. . `mysqlnd` вказує потокам PHP використовувати `mysqlnd.net_read_timeout`. Будь ласка, зверніть увагу, що можуть бути невеликі відмінності між `MYSQL_OPT_READ_TIMEOUT` у клієнтській бібліотеці MySQL та потоках PHP, наприклад, судячи з документації, `MYSQL_OPT_READ_TIMEOUT` працює тільки для TCP/IP-підключень та, аж до MySQL 5.1.2, тільки під Windows. Потоки PHP можуть не мати таких обмежень. У разі сумнівів, прохання звірятися з документацією потоків.

`mysqlnd.net_cmd_buffer_size` int

`mysqlnd` резервує внутрішній командно-мережевий буфер розміром `mysqlnd.net_cmd_buffer_size` (У php.ini) байт для кожного з'єднання. Якщо команда клієнт-серверного протоколу MySQL, наприклад, `COM_QUERY` (звичайний запит), не вміщується в буфер, `mysqlnd` збільшить буфер до розміру, необхідного для надсилання команди. Щоразу, коли буфер був збільшений, змінна статистика `command_buffer_too_small` буде збільшено на один.

Якщо `mysqlnd` доводиться збільшувати буфер понад його заданого розміру `mysqlnd.net_cmd_buffer_size` байт для більшості з'єднань, вам слід обміркувати необхідність збільшення розміру за замовчуванням, щоб уникнути повторних резервацій буфера.

Розмір за замовчуванням буфера становить 4096 байт, що є найменшим можливим значенням.

Це значення також може бути встановлене функцією `mysqli_options(link, MYSQLI_OPT_NET_CMD_BUFFER_SIZE, size)`

`mysqlnd.net_read_buffer_size` int

Максимальний розмір частини даних при зчитуванні в байтах при обробці тіла командного пакета MySQL. Клієнт-серверний протокол MySQL повертає всі свої команди до пакетів. Пакет складається з невеликого заголовка та тіла, що містить безпосередньо дані команди. Розмір тіла закодований у заголовку . `mysqlnd` зчитує тіло частинами по `MIN(header.size, mysqlnd.net_read_buffer_size)` байт. Якщо розмір тіла пакета більший, ніж `mysqlnd.net_read_buffer_size` байт, `mysqlnd` буде викликати `read()` декілька разів.

Це значення також може бути встановлене функцією `mysqli_options(link, MYSQLI_OPT_NET_READ_BUFFER_SIZE, size)`

`mysqlnd.sha256_server_public_key` string

Ця опція відноситься до плагіну автентифікації SHA-256 і містить шлях до файлу з публічним ключем RSA MySQL-сервера.

Клієнт може як не вказувати публічний ключ RSA, вказати його за допомогою цієї опції, або встановити ключ під час виконання за допомогою функції [mysqlioptions()](mysqli.options.html). Якщо публічний ключ RSA не був переданий клієнтом, то ключ буде отримано в результаті стандартної процедури автентифікації плагіну автентифікації SHA-256.

`mysqlnd.trace_alloc` string

`mysqlnd.fetch_data_copy` int

Примушує копіювати набори з внутрішнього буфера наборів PHP змінні замість використання логіки з посиланнями і "копіюванням при записі" за замовчуванням. Дивіться [реализация управления памятью](mysqlnd.memory.html) для більшої інформації.

Копіювання результуючих наборів замість PHP змінних посилаються на них дозволяють виділяти пам'ять для PHP змінних заздалегідь. Залежно від коду користувача, реальних запитів до бази даних і розмірів їх результатів, можна знизити споживання пам'яті mysqlnd.

Не застосовуйте, якщо використовується PDOMySQL. У PDOMySQL ще не додано підтримку цього нового режиму.
