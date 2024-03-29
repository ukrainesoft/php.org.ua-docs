---
navigation:
  - memcached.getbykey.md: '« Memcached::getByKey'
  - memcached.getdelayedbykey.md: 'Memcached::getDelayedByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getDelayed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::getDelayed

(PECL memcached >= 0.1.0)

Memcached::getDelayed — Запитує декілька записів

### Опис

```methodsynopsis
public Memcached::getDelayed(array $keys, bool $with_cas = false, ?callable $value_cb = null): bool
```

**Memcached::getDelayed()** запитує у memcache кілька записів, ключі яких передані в масиві `keys`. Даний метод не чекає відповіді та повертає значення відразу. Коли ви готові отримати записи, зробіть виклик методу [Memcached::fetch()](memcached.fetch.md) або [Memcached::fetchAll()](memcached.fetchall.md). Якщо параметр `with_cas` встановлений у true, то CAS токени також будуть запитані.

Замість отримання результатів у явному вигляді, ви можете вказати [callback-функцію для отримання результату](memcached.callbacks.md)с помощью параметра`value_cb`

### Список параметрів

`keys`

Масив із ключами для запиту записів.

`with_cas`

Чи запитувати CAS токени записів разом зі значеннями.

`value_cb`

Callback-Функция, возвращающая результат, или\*\*`null`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### Приклади

**Приклад #1 Приклад використання** Memcached::getDelayed()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('int', 99);
$m->set('string', 'a simple string');
$m->set('array', array(11, 12));

$m->getDelayed(array('int', 'array'), true);
var_dump($m->fetchAll());
?>
```

Результат виконання наведеного прикладу:

```
array(2) {
  [0]=>
  array(3) {
    ["key"]=>
    string(3) "int"
    ["value"]=>
    int(99)
    ["cas"]=>
    float(2363)
  }
  [1]=>
  array(3) {
    ["key"]=>
    string(5) "array"
    ["value"]=>
    array(2) {
      [0]=>
      int(11)
      [1]=>
      int(12)
    }
    ["cas"]=>
    float(2365)
  }
}
```

### Дивіться також

-   [Memcached::getDelayedByKey()](memcached.getdelayedbykey.md) \- Запитує кілька записів із вказаного сервера
-   [Memcached::fetch()](memcached.fetch.md) \- Витягує наступний результат
-   [Memcached::fetchAll()](memcached.fetchall.md) \- Витягує всі отримані записи
