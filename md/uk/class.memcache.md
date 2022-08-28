Клас Memcache

-   [« Базовое использование](memcache.examples-overview.html)
    
-   [Memcache::add »](memcache.add.html)
    
-   [PHP Manual](index.html)
    
-   [Memcache](book.memcache.html)
    
-   Клас Memcache
    

# Клас Memcache

(PECL memcache >= 0.2.0)

## Вступ

Надає підключення до набору серверів memcache.

## Огляд класів

```classsynopsis



    
     
      class Memcache
     
     {


    
   add(    string $key,    mixed $var,    int $flag = ?,    int $expire = ?): bool
addServer(    string $host,    int $port = 11211,    bool $persistent = ?,    int $weight = ?,    int $timeout = ?,    int $retry_interval = ?,    bool $status = ?,    callable $failure_callback = ?,    int $timeoutms = ?): bool
close(): bool
connect(string $host, int $port = ?, int $timeout = ?): bool
decrement(string $key, int $value = 1): int|false
delete(string $key, int $timeout = 0): bool
flush(): bool
get(string $key, int &$flags = ?): string
getExtendedStats(string $type = ?, int $slabid = ?, int $limit = 100): array
getServerStatus(string $host, int $port = 11211): int
getStats(string $type = ?, int $slabid = ?, int $limit = 100): array|false
getVersion(): string|false
increment(string $key, int $value = 1): int|false
pconnect(string $host, int $port = ?, int $timeout = ?): mixed
replace(    string $key,    mixed $var,    int $flag = ?,    int $expire = ?): bool
set(    string $key,    mixed $var,    int $flag = ?,    int $expire = ?): bool
setCompressThreshold(int $threshold, float $min_savings = ?): bool
setServerParams(    string $host,    int $port = 11211,    int $timeout = ?,    int $retry_interval = false,    bool $status = ?,    callable $failure_callback = ?): bool

   }
```

## Зміст

-   [Memcache::add](memcache.add.html) — Додати елемент із зазначеним ключем
-   [Memcache::addServer](memcache.addserver.html) — Додає сервер memcached у пул з'єднань
-   [Memcache::close](memcache.close.html) — Закрити з'єднання з сервером memcached
-   [Memcache::connect](memcache.connect.html) — Відкриває з'єднання з сервером memcached
-   [Memcache::decrement](memcache.decrement.html) - Декрементувати значення елемента
-   [Memcache::delete](memcache.delete.html) — Видалити елемент із сервера
-   [Memcache::flush](memcache.flush.html) — Скинути всі наявні елементи на сервері
-   [Memcache::get](memcache.get.html) — Вийняти елемент із сервера
-   [Memcache::getExtendedStats](memcache.getextendedstats.html) — Отримати статистику з усіх серверів у пулі
-   [Memcache::getServerStatus](memcache.getserverstatus.html) — Повертає статус сервера
-   [Memcache::getStats](memcache.getstats.html) — Отримати статистику сервера
-   [Memcache::getVersion](memcache.getversion.html) — Повернути версію сервера
-   [Memcache::increment](memcache.increment.html) — Збільшити значення елемента
-   [Memcache::pconnect](memcache.pconnect.html) — Відкриває постійне з'єднання з сервером memcached
-   [Memcache::replace](memcache.replace.html) — Замінити значення наявного елемента
-   [Memcache::set](memcache.set.html) — Зберегти дані на сервері
-   [Memcache::setCompressThreshold](memcache.setcompressthreshold.html) — Увімкнути автоматичний стиск для великих значень
-   [Memcache::setServerParams](memcache.setserverparams.html) — Змінює параметри сервера та статус під час виконання