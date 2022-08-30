Налаштування під час виконання

-   [« Установка](memcached.installation.html)
    
-   [Типы ресурсов »](memcached.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](memcached.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Memcached**

| Имя                                                                                                          | По умолчанию   | Место изменения | Список изменений                                                                             |
|--------------------------------------------------------------------------------------------------------------|----------------|-----------------|----------------------------------------------------------------------------------------------|
| [memcached.sesslocking](memcached.configuration.html#ini.memcached.sess-locking)                             | Він            | PHPINIALL       | Доступно з memcached 0.1.0.                                                                  |
| [memcached.sessconsistenthash](memcached.configuration.html#ini.memcached.sess-consistent-hash)              | Він            | PHPINIALL       | Доступно з memcached 2.1.0. Значення за промовчанням - On, починаючи з memcached 3.0.0.      |
| [memcached.sessbinary](memcached.configuration.html#ini.memcached.sess-binary)                               | Off            | PHPINIALL       | Доступно з memcached 2.0.0. Замінено на memcached.sessbinaryprotocol в memcached 3.0.0.      |
| [memcached.sesslockwait](memcached.configuration.html#ini.memcached.sess-lock-wait)                          |                | PHPINIALL       | Доступно з memcached 0.1.0. Видалено в memcached 3.0.0.                                      |
| [memcached.sessprefix](memcached.configuration.html#ini.memcached.sess-prefix)                               | memc.sess.key. | PHPINIALL       | Доступно з memcached 0.1.0.                                                                  |
| [memcached.sessnumberофreplicas](memcached.configuration.html#ini.memcached.sess-number-of-replicas)         |                | PHPINIALL       | Доступно з memcached 2.1.0.                                                                  |
| [memcached.sessrandomizereplicaread](memcached.configuration.html#ini.memcached.sess-randomize-replica-read) | Off            | PHPINIALL       | Доступно з memcached 2.1.0.                                                                  |
| [memcached.sessremovefailed](memcached.configuration.html#ini.memcached.sess-remove-failed)                  | Він            | PHPINIALL       | Доступно з memcached 2.1.0. Замінено на memcached.sessremovefailedservers в memcached 3.0.0. |
| [memcached.compressiontype](memcached.configuration.html#ini.memcached.compression-type)                     | fastlz         | PHPINIALL       | Доступно з memcached 0.1.0.                                                                  |
| [memcached.compressionfactor](memcached.configuration.html#ini.memcached.compression-factor)                 |                | PHPINIALL       | Доступно з memcached 0.1.0.                                                                  |
| [memcached.compressionthreshold](memcached.configuration.html#ini.memcached.compression-threshold)           |                | PHPINIALL       | Доступно з memcached 0.1.0.                                                                  |
| [memcached.serializer](memcached.configuration.html#ini.memcached.serializer)                                | igbinary       | PHPINIALL       | Доступно з memcached 0.1.0.                                                                  |
| [memcached.usesasl](memcached.configuration.html#ini.memcached.use-sasl)                                     | Off            | PHPINISYSTEM    | Доступно з memcached 2.2.0. Видалено в memcached 3.0.0.                                      |
| [memcached.defaultbinaryprotocol](memcached.configuration.html#ini.memcached.default-binary-protocol)        | Off            | PHPINIALL       | Доступно з memcached 3.0.0.                                                                  |
| [memcached.defaultconnecttimeout](memcached.configuration.html#ini.memcached.default-connect-timeout)        |                | PHPINIALL       | Доступно з memcached 3.0.0.                                                                  |
| [memcached.defaultconsistenthash](memcached.configuration.html#ini.memcached.default-consistent-hash)        | Off            | PHPINIALL       | Доступно з memcached 3.0.0.                                                                  |
| [memcached.sessbinaryprotocol](memcached.configuration.html#ini.memcached.sess-binary-protocol)              | Він            | PHPINIALL       | Доступно з memcached 3.0.0. Замінено на memcached.sessbinary.                                |
| [memcached.sessconnecttimeout](memcached.configuration.html#ini.memcached.sess-connect-timeout)              |                | PHPINIALL       | Доступно з memcached 2.2.0.                                                                  |
| [memcached.sessconsistenthashtype](memcached.configuration.html#ini.memcached.sess-consistent-hash-type)     | ketama         | PHPINIALL       | Доступно з memcached 3.1.0.                                                                  |
| [memcached.sesslockexpire](memcached.configuration.html#ini.memcached.sess-lock-expire)                      |                | PHPINIALL       | Доступно з memcached 2.2.0.                                                                  |
| [memcached.sesslockretries](memcached.configuration.html#ini.memcached.sess-lock-retries)                    |                | PHPINIALL       | Доступно з memcached 3.0.0.                                                                  |
| [memcached.sesslockwaitmax](memcached.configuration.html#ini.memcached.sess-lock-wait-max)                   |                | PHPINIALL       | Доступно з memcached 3.0.0. Значення за замовчуванням 150 з memcached 3.1.0 (вперше 2000).   |
| [memcached.sesslockwaitmin](memcached.configuration.html#ini.memcached.sess-lock-wait-min)                   |                | PHPINIALL       | Доступно з memcached 3.0.0. Значення за замовчуванням 150 з memcached 3.1.0 (вперше 1000).   |
| [memcached.sesspersistent](memcached.configuration.html#ini.memcached.sess-persistent)                       | Off            | PHPINIALL       | Доступно з memcached 3.0.0.                                                                  |
| [memcached.sessremovefailedservers](memcached.configuration.html#ini.memcached.sess-remove-failed-servers)   | Off            | PHPINIALL       | Доступно з memcached 3.0.0. Замінено на memcached.sessremovefailed.                          |
| [memcached.sessserverfailurelimit](memcached.configuration.html#ini.memcached.sess-server-failure-limit)     |                | PHPINIALL       | Доступно з memcached 3.0.0.                                                                  |
| [memcached.sesssaslpassword](memcached.configuration.html#ini.memcached.sess-sasl-password)                  | null           | PHPINIALL       | Доступно з memcached 2.2.0.                                                                  |
| [memcached.sesssaslusername](memcached.configuration.html#ini.memcached.sess-sasl-username)                  | null           | PHPINIALL       | Доступно з memcached 2.2.0.                                                                  |
| [memcached.storeretrycount](memcached.configuration.html#ini.memcached.store-retry-count)                    |                | PHPINIALL       | Доступно з memcached 2.2.0.                                                                  |

Коротке пояснення конфігураційних директив.

`memcached.sess_locking` bool

Використовувати блокування сесій. Допустимі значення: On, Off. За замовчуванням

`memcached.sess_consistent_hash` bool

Якщо увімкнено, то для обробки сесій буде використано узгоджене хешування. У разі використання погодженого хешування можна додавати або видаляти вузли кешування без великих втрат кешованих ключів. За промовчанням On.

`memcached.sess_binary` bool

Використовувати бінарний режим сесії.Репліки libmemcached працюють тільки якщо включений цей режим. За замовчуванням Off.

`memcached.sess_lock_wait` int

Час очікування повторної синхронізації сесії у мікросекундах. Під час встановлення цього значення будьте обережні. Допустимі цілочисельні значення. Якщо встановлено як 0, використовується значення за промовчанням. Негативні значення зменшують блокування спроб блокування. Типово 150000.

`memcached.sess_prefix` string

Префікс ключ сесії. Рядок довжиною трохи більше 219 байт. За промовчанням "memc.sess.key."

`memcached.sess_number_of_replicas` int

Записувати дані на ряд додаткових серверів memcached. Це "висока доступність для бідняків", як її називає libmemcached. Якщо це значення позитивне, і активовано режим sessionsremovefailedservers, коли сервер memcached виходить з ладу, сесія, як і раніше, доступна з репліки. Однак, якщо сервер memcache, що відмовив, знову стає доступним, він буде читати сесію звідти, яка може мати старі дані або взагалі не мати даних. Типово 0.

`memcached.sess_randomize_replica_read` bool

Випадкове читання репліки memcached сесією.

`memcached.sess_remove_failed` int

Дозволити автоматичне видалення недоступних серверів memcached.

`memcached.compression_type` string

Налаштування типу стиснення, коректні значення: fastlz, zlib. Типово fastlz.

`memcached.compression_factor` float

Коефіцієнт стиснення. Зберігати значення стиснутими лише якщо коефіцієнт стиснення перевищує заданий. Зберігаємо стиснутим якщо: `plain_len > comp_len * factor`. Типово 1.3 (економія місця 23%).

`memcached.compression_threshold` int

Поріг стиснення. Не стискати серіалізовані значення менше вказаного розміру. Типово 2000 bytes.

`memcached.serializer` string

Налаштування стандартного серіалізатора для нових об'єктів memcached. Допустимі значення: php, igbinary, json, jsonarray, msgpack.

json

Стандартне кодування JSON. Цей серіалізатор швидкий і компактний, але працює тільки з даними UTF-8 і не повністю реалізує серіалізацію. Подробиці див. у описі модуля JSON. Доступно з memcached 0.2.0.

jsonarray

Те ж json, але розкодується в масиви. Доступно з memcached 2.0.0.

php

Стандартний серіалізатор PHP.

igbinary

Бінарний серіалізатор. Доступно з memcached 0.1.4

msgpack

Міжмовний двійковий серіалізатор. Доступно з memcached 2.2.0.

За замовчуванням igbinary, якщо доступний, потім igbinary, якщо доступний, інакше PHP.

`memcached.use_sasl` bool

Використовувати автентифікацію SASL під час з'єднання. Допустимі значення: On, Off. За замовчуванням Off.

`memcached.default_binary_protocol` bool

Встановлює протокол memcached за промовчанням для нових підключень. (Щоб налаштувати протокол memcached для з'єднань, що використовуються сесіями, використовуйте замість нього memcached.sessbinaryprotocol) Якщо встановлено значення On, за замовчуванням використовується двійковий протокол memcached. Якщо встановлено значення Off, використовується текстовий протокол memcached. За замовчуванням Off

`memcached.default_connect_timeout` int

Встановлює час очікування з'єднання memcached за промовчанням для нових з'єднань. (Щоб налаштувати час очікування з'єднання memcached для сесій, замість цього використовуйте memcached.sessconnecttimeout) У режимі неблокування змінює значення часу очікування під час підключення до сокету в мілісекундах. Вказівка ​​-1 означає нескінченний час очікування. Вказівка ​​0 означає використання часу очікування стандартного з'єднання для бібліотеки memcached. Типово 0.

`memcached.default_consistent_hash` bool

Встановлює значення за промовчанням для узгодженого хешування нових підключень. (Щоб налаштувати узгоджене хешування для сесій, використовуйте натомість memcached.sessconsistenthash) Якщо встановлено значення On, для обробки сесії використовується узгоджене хешування (libketama). Коли використовується узгоджене хешування, можна додавати або видаляти вузли кеша, не турбуючись про те, що ключі за замовчуванням відключені.

`memcached.sess_binary_protocol` bool

Використовуйте двійковий протокол memcached для сесій memcached (замість текстового протоколу). Репліки libmemcached працюють тільки якщо включений двійковий режим. Однак деякі проксі (наприклад, twemproxy) працюватимуть, лише якщо двійковий протокол вимкнено. У старіших версіях php-memcached цей параметр був вимкнений і називався memcached.sessbinary. За замовчуванням включено з libmemcached 1.0.18 або новіше. За промовчанням у старій версії вимкнено.

`memcached.sess_connect_timeout` int

Значення часу очікування з'єднання memcached У режимі, що не блокує, це змінює значення часу очікування під час з'єднання сокету в мілісекундах. Вказівка ​​-1 означає нескінченний час очікування.

`memcached.sess_consistent_hash_type` string

Тип узгодженого хешування сесії Memcached. Якщо встановлено значення 'ketama' (за промовчанням для php-memcached 3.x), для обробки сесії використовується узгоджене хешування libketama, якщо встановлено значення 'ketamaweighted' (за промовчанням для php-memcached 2.x), для обробки сесії використовується зважене узгоджене хешування (libketama). За замовчуванням – "ketama".

`memcached.sess_lock_expire` int

Час у секундах до того, як має спрацювати блокування. Установка в 0 приводить до стандартної поведінки, яка полягає у використанні PHP maxexecutiontime. Типово 0.

`memcached.sess_lock_retries` int

Кількість спроб повторного блокування сесії, не включаючи першу спробу. Типово 5.

`memcached.sess_lock_wait_max` int

Максимальний час очікування у мілісекундах між спробами блокування сесії. Типово 150.

`memcached.sess_lock_wait_min` int

Мінімальний час очікування у мілісекундах між спробами блокування сесії. Це значення подвоюється при кожній спробі блокування доти, доки не буде досягнуто memcached.sesslockwaitmax, після чого будь-які подальші спроби займатимуть sessionslockwaitmax секунд. Типово 150.

`memcached.sess_persistent` bool

Чи слід повторно використовувати з'єднання memcached, що відповідають значенням (значенням) session.savepath після завершення виконання скрипту. Не використовуйте це, якщо певні налаштування (наприклад, SASL, sessbinaryprotocol) будуть перевизначені між запитами. За замовчуванням Off.

`memcached.sess_remove_failed_servers` bool

Дозволити автоматичне видалення сервера, що відмовив, memcached. За замовчуванням Off. (У попередніх версіях цей параметр називався memcached.sessremovefailed)

`memcached.sess_server_failure_limit` int

Встановіть це значення, щоб дозволити видалення сервера після заданої кількості безперервних збоїв підключення. Типово 0.

`memcached.sess_sasl_password` string

Пароль сесії SASL Для включення SASL необхідно вказати ім'я користувача та пароль.

`memcached.sess_sasl_username` string

Ім'я користувача сесії SASL Для включення SASL необхідно вказати ім'я користувача та пароль.

`memcached.store_retry_count` int

Кількість повторних спроб невдалих команд збереження. Цей механізм забезпечує прозоре перемикання на вторинні сервери при збої операцій set/increment/decrement/setMulti на бажаному сервері серед безлічі серверів. за замовчуванням - 2