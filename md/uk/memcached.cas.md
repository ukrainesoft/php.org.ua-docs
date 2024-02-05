---
navigation:
  - memcached.appendbykey.md: '« Memcached::appendByKey'
  - memcached.casbykey.md: 'Memcached::casByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::cas'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::cas

(PECL memcached >= 0.1.0)

Memcached::cas — Порівнює та встановлює значення для запису

### Опис

```methodsynopsis
public Memcached::cas(    string|int|float $cas_token,    string $key,    mixed $value,    int $expiration = 0): bool
```

**Memcached::cas()** здійснює перевірку та встановлення значення запису, нове значення буде збережено тільки якщо інші клієнти не оновили його з часу останнього звернення цим клієнтом. Ця перевірка здійснюється за допомогою параметра `cas_token`, який являє собою 64-бітове значення, присвоєне існуючому запису сервером memcache. Зверніться до документації методу \*\*Memcached::get\*()\*\*який використовується для отримання цього токена. Зверніть увагу, що токен представлений у вигляді числа з плаваючою точкою через обмеження діапазону значень цілого типу в PHP.

### Список параметрів

`cas_token`

Унікальне значення, пов'язане із існуючим записом. Генерується сервером memcache.

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_DATA_EXISTS`** якщо запис, який ви намагаєтеся зберегти, було змінено з моменту останнього звернення.

### Приклади

**Пример #1 Пример использования**Memcached::cas()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

do {
    /* fetch IP list and its token */
    $ips = $m->get('ip_block', null, $cas);
    /* if list doesn't exist yet, create it and do
       an atomic add which will fail if someone else already added it */
    if ($m->getResultCode() == Memcached::RES_NOTFOUND) {
        $ips = array($_SERVER['REMOTE_ADDR']);
        $m->add('ip_block', $ips);
    /* otherwise, add IP to the list and store via compare-and-swap
       with the token, which will fail if someone else updated the list */
    } else {
        $ips[] = $_SERVER['REMOTE_ADDR'];
        $m->cas($cas, 'ip_block', $ips);
    }
} while ($m->getResultCode() != Memcached::RES_SUCCESS);

?>
```

### Дивіться також

-   [Memcached::casByKey()](memcached.casbykey.md) \- Порівнює та встановлює значення для запису на конкретному сервері
