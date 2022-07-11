- [«apcu_cache_info](function.apcu-cache-info.md)
- [apcu_clear_cache »](function.apcu-clear-cache.md)

- [PHP Manual](index.md)
- [Функції APCu](ref.apcu.md)
- Замінює старе значення на нове

#apcu_cas

(PECL apcu \>= 4.0.0)

apcu_cas — Замінює старе значення на нове

### Опис

**apcu_cas**(string `$key`, int `$old`, int `$new`): bool

**apcu_cas()** замінює значення вже існуючого цілісного
значення, якщо воно дорівнює `old` на `new`.

### Список параметрів

`key`
Ключ значення, що змінюється.

`old`
Старе значення (яке зберігається в кеші).

`new`
Нове значення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apcu_cas()****

` <?phpapcu_store('foobar', 2);echo '$foobar = 2', PHP_EOL;echo '$foobar == 1 ? 2 : 1 = ', (apcu_cas('foobar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;echo '$foobar == 2 ? 1 : 2 = ', (apcu_cas('foobar', 2, 1) ? 'ok' : 'fail'), PHP_EOL;echo '$foobar = ', apcu_fetch('foobar')' $; = 1 ? 2 : 1 = ', (apcu_cas('f__bar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;apcu_store('perfection', 'xyz');echo '$perfection ==? 1 : 2 = ', (apcu_cas('perfection', 2, 1) ? 'ok' : 'epic fail'), PHP_EOL;echo '$foobar = ', apcu_fetch(';foo'

Результатом виконання цього прикладу буде щось подібне:

$foobar = 2
$foobar == 1? 2: 1 = fail
$foobar == 2? 1: 2 = ok
$foobar = 1
$f__bar == 1? 2: 1 = fail
$perfection == 2? 1: 2 = epic fail
$foobar = 1

### Дивіться також

- [apcu_dec()](function.apcu-dec.md) - Зменшити збережене число
- [apcu_store()](function.apcu-store.md) - Кешує змінну
