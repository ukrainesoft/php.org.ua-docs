- [« Memcached::fetch](memcached.fetch.md)
- [Memcached::flush »](memcached.flush.md)

- [PHP Manual](index.md)
- [Memcached](class.memcached.md)
- Витягує всі отримані записи

# Memcached::fetchAll

(PECL memcached \>= 0.1.0)

Memcached::fetchAll — Виймає всі отримані записи

### Опис

public **Memcached::fetchAll**(): array\|false

**Memcached::fetchAll()** витягує всі отримані записи останнього
запиту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає результат запиту або **`false`** у разі виникнення
помилки. Використовуйте за необхідності
[Memcached::getResultCode()](memcached.getresultcode.md).

### Приклади

**Приклад #1 Приклад використання
[Memcached::getDelayed()](memcached.getdelayed.md)**

` <?php$m = new Memcached();$m->addServer('localhost', 11211);$m->set('int', 99);$m->set('string', 'a simple string');$m->set('array', array(11, 12));$m->getDelayed(array('int', 'array'), true);var_dump($m->fetchAll ());?> `

Результат виконання цього прикладу:

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

### Дивіться також

- [Memcached::fetch()](memcached.fetch.md) - Витягує наступний
результат
- [Memcached::getDelayed()](memcached.getdelayed.md) - Запитує
кілька записів
