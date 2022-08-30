Отримує кілька записів

-   [« Memcached::getDelayedByKey](memcached.getdelayedbykey.md)
    
-   [Memcached::getMultiByKey »](memcached.getmultibykey.md)
    
-   [PHP Manual](index.md)
    
-   [Memcached](class.memcached.md)
    
-   Отримує кілька записів
    

# Memcached::getMulti

(PECL memcached >= 0.1.0)

Memcached::getMulti — Отримує декілька записів

### Опис

```methodsynopsis
public Memcached::getMulti(array $keys, int $flags = ?): mixed
```

**Memcached::getMulti()** працює аналогічно методу [Memcached::get()](memcached.get.md), але замість одного запису отримує кілька, ключі яких були передані в масиві `keys`

> **Зауваження**
> 
> До версії 3.0 використовувався другий аргумент `&cas_tokens`. Він заповнювався значеннями токена CAS для знайдених записів. Параметр `&cas_tokens` було видалено у версії 3.0. Він був замінений на новий прапор. **`Memcached::GET_EXTENDED`**, який вказується у параметрі `flags`

Параметр `flags` може використовуватися для вказівки додаткових параметрів для методу **Memcached::getMulti()**. На даний момент підтримуються лише наступні налаштування: **`Memcached::GET_PRESERVE_ORDER`** гарантує, що записи будуть повернуті в тому ж порядку, що і були запрошені . **`Memcached::GET_EXTENDED`** веде до того, що також буде вилучено токени CAS.

### Список параметрів

`keys`

Масив ключів для запиту.

`flags`

Прапори для отримання записів.

### Значення, що повертаються

Повертає масив знайдених записів або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.md)

### список змін

| Версия               | Описание                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------------------------------|
| PECL memcached 3.0.0 | Видалено параметр `&cas_tokens`. Додано константу **`Memcached::GET_EXTENDED`** для повернення токенів CAS. |

### Приклади

**Приклад #1 Приклад використання **Memcached::getMulti()** версії 3**

```php
<?php
// Работает с версией модуля 3

$m = new Memcached();
$m->addServer('localhost', 11211);

$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items);
$result = $m->getMulti(array('key1', 'key3', 'badkey'));
var_dump($result);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  ["key1"]=>
  string(6) "value1"
  ["key3"]=>
  string(6) "value3"
}
```

**Приклад #2 Приклад використання **Memcached::getMulti()** версій 1 та 2**

```php
<?php
// Работает с версиями модуля 1 и 2

$m = new Memcached();
$m->addServer('localhost', 11211);

$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items);
$result = $m->getMulti(array('key1', 'key3', 'badkey'), $cas);
var_dump($result, $cas);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  ["key1"]=>
  string(6) "value1"
  ["key3"]=>
  string(6) "value3"
}
array(2) {
  ["key1"]=>
  float(2360)
  ["key3"]=>
  float(2362)
}
```

**Приклад #3 Приклад використання **`Memcached::GET_PRESERVE_ORDER`** з версією 3**

```php
<?php
// Работает с версией модуля 3

$m = new Memcached();
$m->addServer('localhost', 11211);

$data = array(
    'foo' => 'foo-data',
    'bar' => 'bar-data',
    'baz' => 'baz-data',
    'lol' => 'lol-data',
    'kek' => 'kek-data',
);

$m->setMulti($data, 3600);

$keys = array_keys($data);
$keys[] = 'zoo';
$got = $m->getMulti($keys, Memcached::GET_PRESERVE_ORDER);

foreach ($got as $k => $v) {
    echo "$k $v\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
foo foo-data
bar bar-data
baz baz-data
lol lol-data
kek kek-data
zoo
```

**Приклад #4 Приклад використання **`Memcached::GET_PRESERVE_ORDER`** з версією 1 та 2**

```php
<?php
// Работает с версиями модуля 1 и 2

$m = new Memcached();
$m->addServer('localhost', 11211);

$data = array(
    'foo' => 'foo-data',
    'bar' => 'bar-data',
    'baz' => 'baz-data',
    'lol' => 'lol-data',
    'kek' => 'kek-data',
);

$m->setMulti($data, 3600);

$null = null;
$keys = array_keys($data);
$keys[] = 'zoo';
$got = $m->getMulti($keys, $null, Memcached::GET_PRESERVE_ORDER);

foreach ($got as $k => $v) {
    echo "$k $v\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
foo foo-data
bar bar-data
baz baz-data
lol lol-data
kek kek-data
zoo
```

### Дивіться також

-   [Memcached::getMultiByKey()](memcached.getmultibykey.md) - Отримує кілька записів із вказаного сервера
-   [Memcached::get()](memcached.get.md) - Отримання запису
-   [Memcached::getDelayed()](memcached.getdelayed.md) - Запитує кілька записів