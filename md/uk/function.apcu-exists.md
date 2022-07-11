- [«apcu_entry](function.apcu-entry.md)
- [apcu_fetch »](function.apcu-fetch.md)

- [PHP Manual](index.md)
- [Функції APCu](ref.apcu.md)
- Перевіряє, чи є записи

# apcu_exists

(PECL apcu \>= 4.0.0)

apcu_exists — Перевіряє, чи є записи

### Опис

**apcu_exists**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$keys`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Перевіряє, чи є записи.

### Список параметрів

`keys`
Рядок або масив рядків, що містять ключі для перевірки.

### Значення, що повертаються

Повертає **`true`**, якщо ключ існує або **`false`**, якщо ні.
Якщо ж було передано масив ключів, то повернеться масив із існуючими
ключами, або порожній масив, якщо жодного ключа немає.

### Приклади

**Приклад #1 Приклад використання **apcu_exists()****

` <?php$fruit  = 'apple';$veggie = 'carrot';apcu_store('foo', $fruit);apcu_store('bar', $veggie);if (apcu_exists('foo')) {   | Foo с: "; echo apcu_fetch('foo');} else {   echo "Foo не існує";}echo PHP_EOL;if (apcu_exists('baz')) { є|є| }echo PHP_EOL;$ret = apcu_exists(array('foo', 'donotexist', 'bar'));var_dump($ret);?> `

Результатом виконання цього прикладу буде щось подібне:

Foo існує: apple
Baz не існує
array(2) {
["foo"]=>
bool(true)
["bar"]=>
bool(true)
}

### Дивіться також

- [apcu_cache_info()](function.apcu-cache-info.md) - Витягує
закешовану інформацію зі сховища APCu
- [apcu_fetch()](function.apcu-fetch.md) - Витягує з кеша
збережену змінну
