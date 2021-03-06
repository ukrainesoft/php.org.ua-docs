- [«Memcache::add](memcache.add.md)
- [Memcache::close »](memcache.close.md)

- [PHP Manual](index.md)
- [Memcache](class.memcache.md)
- Додає сервер memcached в пул з'єднань

# Memcache::addServer

(PECL memcache \>= 2.0.0)

Memcache::addServer — Додає сервер memcached у пул з'єднань

### Опис

**Memcache::addServer**(
string `$host`,
int `$port` = 11211,
bool `$persistent` = ?,
int `$weight` = ?,
int `$timeout` = ?,
int `$retry_interval` = ?,
bool `$status` = ?,
[callable](language.types.callable.md) `$failure_callback` = ?,
int `$timeoutms` = ?
): bool

**Memcache::addServer()** додає сервер до пулу з'єднань. Ви також
Ви можете використовувати функцію **memcache_add_server()**.

При використанні цього методу (на відміну від
[Memcache::connect()](memcache.connect.md) та
[Memcache::pconnect()](memcache.pconnect.md)) мережне з'єднання не
буде встановлено, поки в ньому не виникне потреби. У зв'язку з цим
можна не побоюватися зниження продуктивності при додаванні великого
кількості серверів в пул, тому що, можливо, вони ніколи не будуть
використані.

Потреба у забезпеченні відмовостійкості може виникнути на будь-якому
етапі в будь-якому методі і якщо при цьому будуть доступні хоча б один сервер
з пулу - користувач не отримає будь-якого сповіщення. Будь-який тип
помилки сокету або сервера Memcached (за винятком помилки переповнення
пам'яті) може увімкнути протокол забезпечення відмовостійкості. Звичайні
клієнтські помилки, такі як додавання існуючого ключа, не викликають
подібної поведінки.

> **Примітка**:
>
> Ця функція була додана до Memcache версії 2.0.0.

### Список параметрів

`host`
Вказує на хост із запущеним сервісом memcached. Цей параметр можна
поставити у вигляді `unix:///path/to/memcached.sock` для використання сокетів
Unix, але в такому випадку необхідно встановити параметр `port`,
рівним `0`.

`port`
Вказує порт, яким доступний сервіс memcached. Необхідно
встановити рівним `0` якщо використовуються сокети Unix.

Будь ласка, зверніть увагу: `port` за замовчуванням дорівнює
[memcache.default_port](memcache.ini.md#ini.memcache.default-port).
Тому рекомендується завжди вказувати номер порту під час використання
цього методу.

`persistent`
Чи використовувати постійне з'єднання. За промовчанням **`true`**.

`weight`
Необхідна кількість створених пакетів даних для цього сервера, що,
своєю чергою, визначає можливість його вибору. Ймовірність
розраховується щодо загальної ваги всіх серверів.

`timeout`
Час очікування в секундах для встановлення з'єднання із сервером. Двічі
подумайте, перш ніж встановлювати це значення більше ніж 1. Це може
нівелювати всю користь від використання memcached.

`retry_interval`
Керує частотою перевірки доступності сервера, що відмовив,
15 секунд. Якщо встановити значення "-1", то спроб перевірити
доступність сервера не буде. Ні цей параметр, ні
параметр `persistent` не впливає, якщо модуль
завантажений динамічно через функцію [dl()](function.dl.md).

Кожна структура з'єднання, що провалилася, має власне значення
часу очікування і, доки воно не перевищено, структура буде пропущена,
після чого спробує вибрати інший сервер обслуговування запиту.
Після того як час з'єднання закінчився, воно або успішно переєднається,
або буде позначено проваленим і чекатиме ще `retry_interval`
секунд. Зазвичай ефект полягає в тому, що кожен процес веб-сервера
буде очікувати `retry_interval` секунд під час обслуговування запиту.

`status`
Визначає, чи сервер позначений прапором як "онлайн". Встановлення
цього параметра в **`false`** та `retry_interval` у -1 дозволить зберегти
сервер у пулі, але не використовувати його в алгоритмі розподілу ключів.
Запит на цей сервер або запустить механізм забезпечення
відмови стійкості, або відразу ж перерветься з помилкою, залежно від
налаштування `memcache.allow_failover`. За умовчанням одно **`true`**, що
означає, що сервер активний та готовий приймати запити.

`failure_callback`
Дозволяє користувачеві встановити функцію зворотного виклику, яка
запуститься у разі будь-якої помилки. Ця функція буде викликана раніше,
чим буде запущено механізм забезпечення стійкості до відмови. Функція
приймає два параметри - ім'я хоста і порт сервера, що відмовив.

`timeoutms`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::addServer()****

`<?php/* об'єктно-орієнтоване API */$memcache = new Memcache;$memcache->addServer('memcache_host', 11211);$memcache->addServer('memcache_host2'  $memcache_obj=memcache_connect('memcache_host', 11211);memcache_add_server($memcache_obj, 'memcache_host2', 11211);?> `

### Примітки

**Увага**

Коли значення `port` не вказано, цей метод використовує значення,
вказане в ini-директиві PHP
[memcache.default_port](memcache.ini.md#ini.memcache.default-port).
Якщо це значення було змінено десь у вашому додатку, то
це може дати непередбачувані результати. З цієї причини краще завжди
явно вказувати порт під час виклику методу.

### Дивіться також

- [Memcache::connect()](memcache.connect.md) - Відкриває з'єднання
з сервером memcached
- [Memcache::pconnect()](memcache.pconnect.md) - Відкриває
постійне з'єднання з сервером memcached
- [Memcache::close()](memcache.close.md) - Закрити з'єднання з
сервером memcached
- [Memcache::setServerParams()](memcache.setserverparams.md) -
Змінює параметри сервера та статус під час виконання
- [Memcache::getServerStatus()](memcache.getserverstatus.md) -
Повертає статус сервера
