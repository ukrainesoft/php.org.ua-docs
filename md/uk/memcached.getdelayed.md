Запитує кілька записів

-   [« Memcached::getByKey](memcached.getbykey.html)
    
-   [Memcached::getDelayedByKey »](memcached.getdelayedbykey.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Запитує кілька записів
    

# Memcached::getDelayed

(PECL memcached >= 0.1.0)

Memcached::getDelayed — Запитує декілька записів

### Опис

```methodsynopsis
public Memcached::getDelayed(array $keys, bool $with_cas = ?, callable $value_cb = ?): bool
```

**Memcached::getDelayed()** запитує у memcache кілька записів, ключі яких передані в масиві `keys`. Даний метод не чекає відповіді та повертає значення відразу. Коли ви готові отримати записи, зробіть виклик методу [Memcached::fetch()](memcached.fetch.html) або [Memcached::fetchAll()](memcached.fetchall.html). Якщо параметр `with_cas` встановлений у true, то CAS токени також будуть запитані.

Замість отримання результатів у явному вигляді, ви можете вказати [callback-функцию для получения результата](memcached.callbacks.html) за допомогою параметра `value_cb`

### Список параметрів

`keys`

Масив із ключами для запиту записів.

`with_cas`

Чи запитувати CAS токени записів разом зі значеннями.

`value_cb`

Callback-Функція, що повертає результат, або **`null`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.html)

### Приклади

**Приклад #1 Приклад використання **Memcached::getDelayed()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('int', 99);
$m->set('string', 'a simple string');
$m->set('array', array(11, 12));

$m->getDelayed(array('int', 'array'), true);
var_dump($m->fetchAll());
?>
```

Результат виконання цього прикладу:

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

-   [Memcached::getDelayedByKey()](memcached.getdelayedbykey.html) - Запитує кілька записів із вказаного сервера
-   [Memcached::fetch()](memcached.fetch.html) - Витягує наступний результат
-   [Memcached::fetchAll()](memcached.fetchall.html) - Витягує всі отримані записи