- [« Memcached::getByKey](memcached.getbykey.md)
- [Memcached::getDelayedByKey »](memcached.getdelayedbykey.md)

- [PHP Manual](index.md)
- [Memcached](class.memcached.md)
- запитує кілька записів

# Memcached::getDelayed

(PECL memcached \>= 0.1.0)

Memcached::getDelayed — Запитує кілька записів

### Опис

public **Memcached::getDelayed**(array `$keys`, bool `$with_cas` = ?,
[callable](language.types.callable.md) $value_cb = ?): bool

**Memcached::getDelayed()** запитує у memcache кілька записів,
ключі яких передані в масиві `keys`. Цей метод не чекає
відповіді та повертає значення відразу. Коли ви будете готові отримати
запису, зробіть виклик методу [Memcached::fetch()](memcached.fetch.md)
або [Memcached::fetchAll()](memcached.fetchall.md). Якщо параметр
`with_cas` встановлено в true, то CAS токени також будуть запрошені.

Замість отримання результатів у явному вигляді, ви можете вказати
[callback-функцію для отримання результату](memcached.callbacks.md) з
за допомогою параметра `value_cb`.

### Список параметрів

`keys`
Масив із ключами для запиту записів.

`with_cas`
Чи запитувати CAS токени записів разом зі значеннями.

`value_cb`
Callback-Функція, що повертає результат, або **`null`**.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки. Використовуйте за необхідності
[Memcached::getResultCode()](memcached.getresultcode.md).

### Приклади

**Приклад #1 Приклад використання **Memcached::getDelayed()****

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

- [Memcached::getDelayedByKey()](memcached.getdelayedbykey.md) -
Запитує кілька записів із вказаного сервера
- [Memcached::fetch()](memcached.fetch.md) - Витягує наступний
результат
- [Memcached::fetchAll()](memcached.fetchall.md) - Витягує все
отримані записи
