---
navigation:
  - memcached.callbacks.result.md: « Функції зворотного дзвінка для результуючого набору
  - memcached.sessions.md: Підтримка сесій »
  - index.md: PHP Manual
  - memcached.callbacks.md: Функції зворотного дзвінка
title: Функції зворотного виклику наскрізного читання кеша
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Функції зворотного виклику наскрізного читання кеша

Дані функції викликаються у разі, коли неможливо отримати потрібне значення. У функцію зворотного дзвінка передається об'єкт Memcached та запитаний ключ, а також передається за посиланням змінна для повернення значення. Функція має повернути **`false`** або **`true`**. Якщо **`true`**, то Memcached збереже отримане значення і поверне його оригінальну функцію. Дані функції зворотного дзвінка використовуються тільки з [Memcached::get()](memcached.get.md) і [Memcached::getByKey()](memcached.getbykey.md), оскільки протокол не надає інформації про те, яких ключів не знайдено, при пакетних запитах.

**Приклад #1 Приклад використання**

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$profile_info = $m->get('user:'.$user_id, 'user_info_cb');

function user_info_cb($memc, $key, &$value)
{
    $user_id = substr($key, 5);
    /* ищем необходимые данные в БД */
    /* ... */
    $value = $profile_info;
    return true;
}
?>
```
