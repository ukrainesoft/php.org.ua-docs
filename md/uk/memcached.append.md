Додає дані до існуючого запису

-   [« Memcached::addServers](memcached.addservers.html)
    
-   [Memcached::appendByKey »](memcached.appendbykey.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Додає дані до існуючого запису
    

# Memcached::append

(PECL memcached >= 0.1.0)

Memcached::append — Додає дані до існуючого запису

### Опис

```methodsynopsis
public Memcached::append(string $key, string $value): bool
```

**Memcached::append()** додає передану в `value` рядок до існуючого запису. Причина того, що `value` наводиться рядок у тому, що додавання змішаних типів не визначено.

> **Зауваження**
> 
> Якщо параметр **`Memcached::OPT_COMPRESSION`** встановлений, то операція буде завершена помилкою і буде виведено попередження, тому що додавання стислих даних до запису, який вже стислий, неможливо.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Рядок для додавання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає **`Memcached::RES_NOTSTORED`**, якщо переданий ключ не існує.

### Приклади

**Приклад #1 Приклад використання **Memcached::append()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$m->setOption(Memcached::OPT_COMPRESSION, false);

$m->set('foo', 'abc');
$m->append('foo', 'def');
var_dump($m->get('foo'));
?>
```

Результат виконання цього прикладу:

```
string(6) "abcdef"
```

### Дивіться також

-   [Memcached::appendByKey()](memcached.appendbykey.html) - Додає дані до наявного запису на заданому сервері
-   [Memcached::prepend()](memcached.prepend.html) - Додає дані на початок існуючого запису