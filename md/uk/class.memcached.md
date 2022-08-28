Клас Memcached

-   [« Поддержка сессий](memcached.sessions.html)
    
-   [Memcached::add »](memcached.add.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](book.memcached.html)
    
-   Клас Memcached
    

# Клас Memcached

(PECL memcached >= 0.1.0)

## Вступ

Представляє з'єднання до набору серверів memcached.

## Огляд класів

```classsynopsis


    
    
     
      class Memcached
     
     {
    

    
   public __construct(string $persistent_id = ?)

    public add(string $key, mixed $value, int $expiration = ?): bool
public addByKey(    string $server_key,    string $key,    mixed $value,    int $expiration = ?): bool
public addServer(string $host, int $port, int $weight = 0): bool
public addServers(array $servers): bool
public append(string $key, string $value): bool
public appendByKey(string $server_key, string $key, string $value): bool
public cas(    float $cas_token,    string $key,    mixed $value,    int $expiration = ?): bool
public casByKey(    float $cas_token,    string $server_key,    string $key,    mixed $value,    int $expiration = ?): bool
public decrement(    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
public decrementByKey(    string $server_key,    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
public delete(string $key, int $time = 0): bool
public deleteByKey(string $server_key, string $key, int $time = 0): bool
public deleteMulti(array $keys, int $time = 0): array
public deleteMultiByKey(string $server_key, array $keys, int $time = 0): bool
public fetch(): array
public fetchAll(): array|false
public flush(int $delay = 0): bool
public get(string $key, callable $cache_cb = ?, int $flags = ?): mixed
public getAllKeys(): array|false
public getByKey(    string $server_key,    string $key,    callable $cache_cb = ?,    int $flags = ?): mixed
public getDelayed(array $keys, bool $with_cas = ?, callable $value_cb = ?): bool
public getDelayedByKey(    string $server_key,    array $keys,    bool $with_cas = ?,    callable $value_cb = ?): bool
public getMulti(array $keys, int $flags = ?): mixed
public getMultiByKey(string $server_key, array $keys, int $flags = ?): array|false
public getOption(int $option): mixed
public getResultCode(): int
public getResultMessage(): string
public getServerByKey(string $server_key): array
public getServerList(): array
public getStats(): array|false
public getVersion(): array
public increment(    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
public incrementByKey(    string $server_key,    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
public isPersistent(): bool
public isPristine(): bool
public prepend(string $key, string $value): bool
public prependByKey(string $server_key, string $key, string $value): bool
public quit(): bool
public replace(string $key, mixed $value, int $expiration = ?): bool
public replaceByKey(    string $server_key,    string $key,    mixed $value,    int $expiration = ?): bool
public resetServerList(): bool
public set(string $key, mixed $value, int $expiration = ?): bool
public setByKey(    string $server_key,    string $key,    mixed $value,    int $expiration = ?): bool
public setMulti(array $items, int $expiration = ?): bool
public setMultiByKey(string $server_key, array $items, int $expiration = ?): bool
public setOption(int $option, mixed $value): bool
public setOptions(array $options): bool
public setSaslAuthData(string $username, string $password): void
public touch(string $key, int $expiration): bool
public touchByKey(string $server_key, string $key, int $expiration): bool

   }
```

## Зміст

-   [Memcached::add](memcached.add.html) — Додає елемент із новим ключем
-   [Memcached::addByKey](memcached.addbykey.html) — Додає новий елемент на заданий сервер
-   [Memcached::addServer](memcached.addserver.html) — Додає сервер у пул
-   [Memcached::addServers](memcached.addservers.html) — Додає кілька серверів у пул
-   [Memcached::append](memcached.append.html) — Додає дані до наявного запису
-   [Memcached::appendByKey](memcached.appendbykey.html) — Додає дані до наявного запису на заданому сервері
-   [Memcached::cas](memcached.cas.html) — Порівнює та встановлює значення для запису
-   [Memcached::casByKey](memcached.casbykey.html) — Порівнює та встановлює значення для запису на конкретному сервері
-   [Memcached::\_\_construct](memcached.construct.html) - Створює екземпляр класу Memcached
-   [Memcached::decrement](memcached.decrement.html) — Зменшує числове значення запису
-   [Memcached::decrementByKey](memcached.decrementbykey.html) — Зменшує числове значення запису, що зберігається на певному сервері
-   [Memcached::delete](memcached.delete.html) - Видаляє запис
-   [Memcached::deleteByKey](memcached.deletebykey.html) — Видаляє запис із вказаного сервера
-   [Memcached::deleteMulti](memcached.deletemulti.html) - Видаляє кілька записів
-   [Memcached::deleteMultiByKey](memcached.deletemultibykey.html) — Видаляє кілька записів із вказаного сервера
-   [Memcached::fetch](memcached.fetch.html) — Витягує наступний результат
-   [Memcached::fetchAll](memcached.fetchall.html) — Витягує всі отримані записи
-   [Memcached::flush](memcached.flush.html) — Анулює всі записи у кеші
-   [Memcached::get](memcached.get.html) — Отримання запису
-   [Memcached::getAllKeys](memcached.getallkeys.html) — Отримує всі ключі, що зберігаються на серверах
-   [Memcached::getByKey](memcached.getbykey.html) — Отримує запис із певного сервера
-   [Memcached::getDelayed](memcached.getdelayed.html) — Запитує кілька записів
-   [Memcached::getDelayedByKey](memcached.getdelayedbykey.html) — Запитує кілька записів із вказаного сервера
-   [Memcached::getMulti](memcached.getmulti.html) — Отримує кілька записів
-   [Memcached::getMultiByKey](memcached.getmultibykey.html) — Отримує кілька записів із вказаного сервера
-   [Memcached::getOption](memcached.getoption.html) — Отримує значення Memcached параметра
-   [Memcached::getResultCode](memcached.getresultcode.html) — Повертає результуючий код останньої виконаної операції
-   [Memcached::getResultMessage](memcached.getresultmessage.html) — Повертає повідомлення, яке описує результат виконання останньої операції
-   [Memcached::getServerByKey](memcached.getserverbykey.html) — Отримує інформацію про сервер за ключом
-   [Memcached::getServerList](memcached.getserverlist.html) — Отримує список серверів у пулі
-   [Memcached::getStats](memcached.getstats.html) — Отримує статистику про сервери в пулі
-   [Memcached::getVersion](memcached.getversion.html) — Отримує інформацію про версію серверів у пулі
-   [Memcached::increment](memcached.increment.html) — Збільшує числове значення запису
-   [Memcached::incrementByKey](memcached.incrementbykey.html) — Збільшує числове значення запису, що зберігається на вказаному сервері
-   [Memcached::isPersistent](memcached.ispersistent.html) — Перевіряє, чи використовується стійке з'єднання з сервером memcache
-   [Memcached::isPristine](memcached.ispristine.html) — Перевіряє чи вже створено екземпляр класу Memcached
-   [Memcached::prepend](memcached.prepend.html) — Додає дані на початок існуючого запису
-   [Memcached::prependByKey](memcached.prependbykey.html) — Додає дані на початок існуючого запису на вказаному сервері
-   [Memcached::quit](memcached.quit.html) — Закриває всі відкриті з'єднання
-   [Memcached::replace](memcached.replace.html) — Замінює існуючий запис із зазначеним ключем
-   [Memcached::replaceByKey](memcached.replacebykey.html) — Замінює існуючий запис із заданим ключем на вказаному сервері
-   [Memcached::resetServerList](memcached.resetserverlist.html) — Очищає список серверів
-   [Memcached::set](memcached.set.html) - Зберігає запис
-   [Memcached::setByKey](memcached.setbykey.html) — Зберігає запис на вказаному сервері
-   [Memcached::setMulti](memcached.setmulti.html) — Зберігає кілька записів
-   [Memcached::setMultiByKey](memcached.setmultibykey.html) — Зберігає кілька записів на вказаному сервері
-   [Memcached::setOption](memcached.setoption.html) — Встановлює параметр для Memcached
-   [Memcached::setOptions](memcached.setoptions.html) — Встановлює кілька параметрів Memcached
-   [Memcached::setSaslAuthData](memcached.setsaslauthdata.html) — Встановлює облікові дані для автентифікації
-   [Memcached::touch](memcached.touch.html) — Встановлює новий термін зберігання для запису
-   [Memcached::touchByKey](memcached.touchbykey.html) — Встановлює новий термін зберігання для запису на вказаному сервері