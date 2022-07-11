- [« Memcached::getDelayedByKey](memcached.getdelayedbykey.md)
- [Memcached::getMultiByKey »](memcached.getmultibykey.md)

- [PHP Manual](index.md)
- [Memcached](class.memcached.md)
- Отримує кілька записів

# Memcached::getMulti

(PECL memcached \>= 0.1.0)

Memcached::getMulti — Отримує кілька записів

### Опис

public **Memcached::getMulti**(array `$keys`, int `$flags` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

**Memcached::getMulti()** працює аналогічно методу
[Memcached::get()](memcached.get.md), але замість одного запису отримує
кілька, ключі яких були передані в масиві `keys`.

> **Примітка**:
>
> До версії 3.0 використовувався другий аргумент `&cas_tokens`. Він
> заповнювався значеннями токена CAS для знайдених записів. Параметр
> `&cas_tokens` було видалено у версії 3.0. Він був замінений на новий прапор.
> **`Memcached::GET_EXTENDED`**, який вказується у параметрі
> `flags`.

Параметр `flags` може використовуватись для вказівки додаткових
налаштувань для методу **Memcached::getMulti()**. На даний момент
підтримуються лише наступні настройки:
**`Memcached::GET_PRESERVE_ORDER`** гарантує що записи будуть
повернені в тому ж порядку, що були запрошені.
**`Memcached::GET_EXTENDED`** веде до того, що також будуть вилучені
токени CAS.

### Список параметрів

`keys`
Масив ключів для запиту.

`flags`
Прапори для отримання записів.

### Значення, що повертаються

Повертає масив знайдених записів або **`false`** у разі
виникнення помилки. Використовуйте за необхідності
[Memcached::getResultCode()](memcached.getresultcode.md).

### Список змін

| Версія               | Опис                                                                                                    |
| -------------------- | ------------------------------------------------------------------------------------------------------- |
| PECL memcached 3.0.0 | Видалено параметр &cas_tokens. Додано константу **Memcached::GET_EXTENDED** для повернення токенів CAS. |

### Приклади

**Приклад #1 Приклад використання **Memcached::getMulti()** версії 3**

`<?php// Працює з версією модуля 3$m = new Memcached();$m->addServer('localhost', 11211);$items = array( val>           > 'value2',   'key3' => 'value3');$m->setMulti($items);$result = $m->getMulti(array('key1', 'key3', 'badkey')); var_dump($result);?> `

Результатом виконання цього прикладу буде щось подібне:

array(2) {
["key1"]=>
string(6) "value1"
["key3"]=>
string(6) "value3"
}

**Приклад #2 Приклад використання **Memcached::getMulti()** версій 1 та
2**

`<?php// Працює з версіями модуля 1 і 2$m = new Memcached();$m->addServer('localhost', 11211);$items =1 array(     ' => 'value2',   'key3' => 'value3');$m->setMulti($items);$result = $m->getMulti(array('key1', 'key3', 'badkey') , $cas);var_dump($result, $cas);?> `

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #3 Приклад використання **`Memcached::GET_PRESERVE_ORDER`** з
версією 3**

`<?php// Працює з версією модуля 3$m = new Memcached();$m->addServer('localhost', 11211);$data = array(  - ta ' => 'bar-data',   'baz' => 'baz-data',   'lol' => 'lol-data',   'kek' => 'kek-data',);$m-set $data, 3600);$keys = array_keys($data);$keys[] = 'zoo';$got = $m->getMulti($keys, Memcached::GET_PRESERVE_ORDER);foreach ($got > $v) {   echo "$k $v
";}?> `

Результатом виконання цього прикладу буде щось подібне:

foo foo-data
bar bar-data
baz baz-data
lol lol-data
kek kek-data
zoo

**Приклад #4 Приклад використання **`Memcached::GET_PRESERVE_ORDER`** з
версією 1 та 2**

` <?php// Працює з версіями модуля 1 і 2$m = new Memcached();$m->addServer('localhost', 11211);$data = array(  o'' 'bar' => 'bar-data',    'baz' => 'baz-data',   'lol' => 'lol-data',   ''ekek' => 'kek-data',); setMulti($data, 3600);$null = null;$keys = array_keys($data);$keys[] = 'zoo';$got = $m->getMulti($keys, $null, Memcached::E );foreach ($got as $k => $v) {    echo "$k $v
";}?> `

Результатом виконання цього прикладу буде щось подібне:

foo foo-data
bar bar-data
baz baz-data
lol lol-data
kek kek-data
zoo

### Дивіться також

- [Memcached::getMultiByKey()](memcached.getmultibykey.md) -
Отримує кілька записів із вказаного сервера
- [Memcached::get()](memcached.get.md) - Отримання запису
- [Memcached::getDelayed()](memcached.getdelayed.md) - Запитує
кілька записів
