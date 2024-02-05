---
navigation:
  - memcached.cas.md: '« Memcached::cas'
  - memcached.construct.md: 'Memcached::\_\_construct »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::casByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::casByKey

(PECL memcached >= 0.1.0)

Memcached::casByKey — Порівнює та встановлює значення для запису на конкретному сервері

### Опис

```methodsynopsis
public Memcached::casByKey(    string|int|float $cas_token,    string $server_key,    string $key,    mixed $value,    int $expiration = 0): bool
```

**Memcached::casByKey()** працює аналогічно методу [Memcached::cas()](memcached.cas.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та установки `key` на конкретний сервер. Це корисно, коли необхідно тримати кілька пов'язаних значень на конкретному сервері.

### Список параметрів

`cas_token`

Унікальне значення, пов'язане із існуючим записом. Генерується сервером memcache.

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_DATA_EXISTS`** якщо запис, який ви намагаєтеся зберегти, було змінено з моменту останнього звернення.

### Дивіться також

-   [Memcached::cas()](memcached.cas.md) \- Порівнює та встановлює значення для запису
