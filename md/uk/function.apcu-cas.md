Замінює старе значення на нове

-   [« apcucacheinfo](function.apcu-cache-info.html)
    
-   [apcuclearcache »](function.apcu-clear-cache.html)
    
-   [PHP Manual](index.html)
    
-   [Функции APCu](ref.apcu.html)
    
-   Замінює старе значення на нове
    

# apcucas

(PECL apcu >= 4.0.0)

apcucas — Замінює старе значення на нове

### Опис

```methodsynopsis
apcu_cas(string $key, int $old, int $new): bool
```

**apcucas()** замінює значення вже існуючого цілого чисельного значення, якщо воно дорівнює `old` на `new`

### Список параметрів

`key`

Ключ значення, що змінюється.

`old`

Старе значення (яке зараз зберігається в кеші).

`new`

Нове значення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apcucas()****

```php
<?php
apcu_store('foobar', 2);
echo '$foobar = 2', PHP_EOL;
echo '$foobar == 1 ? 2 : 1 = ', (apcu_cas('foobar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;
echo '$foobar == 2 ? 1 : 2 = ', (apcu_cas('foobar', 2, 1) ? 'ok' : 'fail'), PHP_EOL;

echo '$foobar = ', apcu_fetch('foobar'), PHP_EOL;

echo '$f__bar == 1 ? 2 : 1 = ', (apcu_cas('f__bar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;

apcu_store('perfection', 'xyz');
echo '$perfection == 2 ? 1 : 2 = ', (apcu_cas('perfection', 2, 1) ? 'ok' : 'epic fail'), PHP_EOL;

echo '$foobar = ', apcu_fetch('foobar'), PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
$foobar = 2
$foobar == 1 ? 2 : 1 = fail
$foobar == 2 ? 1 : 2 = ok
$foobar = 1
$f__bar == 1 ? 2 : 1 = fail
$perfection == 2 ? 1 : 2 = epic fail
$foobar = 1
```

### Дивіться також

-   [apcudec()](function.apcu-dec.html) - Зменшити збережене число
-   [apcustore()](function.apcu-store.html) - Кешує змінну