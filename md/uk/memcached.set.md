---
navigation:
  - memcached.resetserverlist.md: '« Memcached::resetServerList'
  - memcached.setbykey.md: 'Memcached::setByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::set

(PECL memcached >= 0.1.0)

Memcached::set — Зберігає запис

### Опис

```methodsynopsis
public Memcached::set(string $key, mixed $value, int $expiration = 0): bool
```

**Memcached::set()** зберігає значення `value` на memcache сервері під вказаним ключем `key`Параметр`expiration` може бути використаний контролю, коли термін дії значення вважається минулим.

Значення може бути будь-яким доступним типом PHP, крім ресурсу, тому що цей тип не може бути представлений в серіалізованому вигляді. Якщо встановлено параметр **`Memcached::OPT_COMPRESSION`**, то серіалізоване значення також буде стиснуто перед збереженням.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### Приклади

**Пример #1 Пример использования**Memcached::set()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('int', 99);
$m->set('string', 'a simple string');
$m->set('array', array(11, 12));
/* время хранения записи с ключом 'object' установлено в 5 минут */
$m->set('object', new stdClass, time() + 300);


var_dump($m->get('int'));
var_dump($m->get('string'));
var_dump($m->get('array'));
var_dump($m->get('object'));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(99)
string(15) "a simple string"
array(2) {
  [0]=>
  int(11)
  [1]=>
  int(12)
}
object(stdClass)#1 (0) {
}
```

### Дивіться також

-   [Memcached::setByKey()](memcached.setbykey.md) \- Зберігає запис на вказаному сервері
-   [Memcached::add()](memcached.add.md) \- Додає елемент із новим ключем
-   [Memcached::replace()](memcached.replace.md) \- Замінює існуючий запис із зазначеним ключем
