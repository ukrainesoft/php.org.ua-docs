---
navigation:
  - memcache.examples-overview.md: « Базове використання
  - memcache.add.md: 'Memcache::add »'
  - index.md: PHP Manual
  - book.memcache.md: Memcache
title: Клас Memcache
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [Memcache::add](memcache.add.md)— Додати елемент із зазначеним ключем
-   [Memcache::addServer](memcache.addserver.md)— Додає сервер memcached у пул з'єднань
-   [Memcache::close](memcache.close.md)— Закрити з'єднання з сервером memcached
-   [Memcache::connect](memcache.connect.md)— Відкриває з'єднання з сервером memcached
-   [Memcache::decrement](memcache.decrement.md) \- Декрементувати значення елемента
-   [Memcache::delete](memcache.delete.md)— Видалити елемент із сервера
-   [Memcache::flush](memcache.flush.md)— Скинути всі наявні елементи на сервері
-   [Memcache::get](memcache.get.md)— Вийняти елемент із сервера
-   [Memcache::getExtendedStats](memcache.getextendedstats.md)— Отримати статистику з усіх серверів у пулі
-   [Memcache::getServerStatus](memcache.getserverstatus.md)— Повертає статус сервера
-   [Memcache::getStats](memcache.getstats.md)— Отримати статистику сервера
-   [Memcache::getVersion](memcache.getversion.md)— Повернути версію сервера
-   [Memcache::increment](memcache.increment.md)— Збільшити значення елемента
-   [Memcache::pconnect](memcache.pconnect.md)— Відкриває постійне з'єднання з сервером memcached
-   [Memcache::replace](memcache.replace.md)— Замінити значення наявного елемента
-   [Memcache::set](memcache.set.md)— Зберегти дані на сервері
-   [Memcache::setCompressThreshold](memcache.setcompressthreshold.md)— Увімкнути автоматичний стиск для великих значень
-   [Memcache::setServerParams](memcache.setserverparams.md)— Змінює параметри сервера та статус під час виконання
