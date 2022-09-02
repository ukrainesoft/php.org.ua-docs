---
navigation:
  - memcached.sessions.md: « Поддержка сессий
  - memcached.add.md: 'Memcached::add »'
  - index.md: PHP Manual
  - book.memcached.md: Memcached
title: Клас Memcached
---
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

-   [Memcached::add](memcached.add.md) — Додає елемент із новим ключем
-   [Memcached::addByKey](memcached.addbykey.md) — Додає новий елемент на заданий сервер
-   [Memcached::addServer](memcached.addserver.md) — Додає сервер у пул
-   [Memcached::addServers](memcached.addservers.md) — Додає кілька серверів у пул
-   [Memcached::append](memcached.append.md) — Додає дані до наявного запису
-   [Memcached::appendByKey](memcached.appendbykey.md) — Додає дані до наявного запису на заданому сервері
-   [Memcached::cas](memcached.cas.md) — Порівнює та встановлює значення для запису
-   [Memcached::casByKey](memcached.casbykey.md) — Порівнює та встановлює значення для запису на конкретному сервері
-   [Memcached::construct](memcached.construct.md) - Створює екземпляр класу Memcached
-   [Memcached::decrement](memcached.decrement.md) — Зменшує числове значення запису
-   [Memcached::decrementByKey](memcached.decrementbykey.md) — Зменшує числове значення запису, що зберігається на певному сервері
-   [Memcached::delete](memcached.delete.md) - Видаляє запис
-   [Memcached::deleteByKey](memcached.deletebykey.md) — Видаляє запис із вказаного сервера
-   [Memcached::deleteMulti](memcached.deletemulti.md) - Видаляє кілька записів
-   [Memcached::deleteMultiByKey](memcached.deletemultibykey.md) — Видаляє кілька записів із вказаного сервера
-   [Memcached::fetch](memcached.fetch.md) — Витягує наступний результат
-   [Memcached::fetchAll](memcached.fetchall.md) — Витягує всі отримані записи
-   [Memcached::flush](memcached.flush.md) — Анулює всі записи у кеші
-   [Memcached::get](memcached.get.md) — Отримання запису
-   [Memcached::getAllKeys](memcached.getallkeys.md) — Отримує всі ключі, що зберігаються на серверах
-   [Memcached::getByKey](memcached.getbykey.md) — Отримує запис із певного сервера
-   [Memcached::getDelayed](memcached.getdelayed.md) — Запитує кілька записів
-   [Memcached::getDelayedByKey](memcached.getdelayedbykey.md) — Запитує кілька записів із вказаного сервера
-   [Memcached::getMulti](memcached.getmulti.md) — Отримує кілька записів
-   [Memcached::getMultiByKey](memcached.getmultibykey.md) — Отримує кілька записів із вказаного сервера
-   [Memcached::getOption](memcached.getoption.md) — Отримує значення Memcached параметра
-   [Memcached::getResultCode](memcached.getresultcode.md) — Повертає результуючий код останньої виконаної операції
-   [Memcached::getResultMessage](memcached.getresultmessage.md) — Повертає повідомлення, яке описує результат виконання останньої операції
-   [Memcached::getServerByKey](memcached.getserverbykey.md) — Отримує інформацію про сервер за ключом
-   [Memcached::getServerList](memcached.getserverlist.md) — Отримує список серверів у пулі
-   [Memcached::getStats](memcached.getstats.md) — Отримує статистику про сервери в пулі
-   [Memcached::getVersion](memcached.getversion.md) — Отримує інформацію про версію серверів у пулі
-   [Memcached::increment](memcached.increment.md) — Збільшує числове значення запису
-   [Memcached::incrementByKey](memcached.incrementbykey.md) — Збільшує числове значення запису, що зберігається на вказаному сервері
-   [Memcached::isPersistent](memcached.ispersistent.md) — Перевіряє, чи використовується стійке з'єднання з сервером memcache
-   [Memcached::isPristine](memcached.ispristine.md) — Перевіряє чи вже створено екземпляр класу Memcached
-   [Memcached::prepend](memcached.prepend.md) — Додає дані на початок існуючого запису
-   [Memcached::prependByKey](memcached.prependbykey.md) — Додає дані на початок існуючого запису на вказаному сервері
-   [Memcached::quit](memcached.quit.md) — Закриває всі відкриті з'єднання
-   [Memcached::replace](memcached.replace.md) — Замінює існуючий запис із зазначеним ключем
-   [Memcached::replaceByKey](memcached.replacebykey.md) — Замінює існуючий запис із заданим ключем на вказаному сервері
-   [Memcached::resetServerList](memcached.resetserverlist.md) — Очищає список серверів
-   [Memcached::set](memcached.set.md) - Зберігає запис
-   [Memcached::setByKey](memcached.setbykey.md) — Зберігає запис на вказаному сервері
-   [Memcached::setMulti](memcached.setmulti.md) — Зберігає кілька записів
-   [Memcached::setMultiByKey](memcached.setmultibykey.md) — Зберігає кілька записів на вказаному сервері
-   [Memcached::setOption](memcached.setoption.md) — Встановлює параметр для Memcached
-   [Memcached::setOptions](memcached.setoptions.md) — Встановлює кілька параметрів Memcached
-   [Memcached::setSaslAuthData](memcached.setsaslauthdata.md) — Встановлює облікові дані для автентифікації
-   [Memcached::touch](memcached.touch.md) — Встановлює новий термін зберігання для запису
-   [Memcached::touchByKey](memcached.touchbykey.md) — Встановлює новий термін зберігання для запису на вказаному сервері
