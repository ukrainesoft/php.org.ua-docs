---
navigation:
  - function.apcu-cache-info.md: « apcu\_cache\_info
  - function.apcu-clear-cache.md: apcu\_clear\_cache »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_cas
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_cas

(PECL apcu >= 4.0.0)

apcu\_cas — Замінює старе значення на нове

### Опис

```methodsynopsis
apcu_cas(string $key, int $old, int $new): bool
```

**apcu\_cas()** замінює значення вже існуючого цілого чисельного значення, якщо воно дорівнює `old`на`new`

### Список параметрів

`key`

Ключ значення, що змінюється.

`old`

Старе значення (яке зараз зберігається в кеші).

`new`

Нове значення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**apcu\_cas()\*\*\*\*

```php
<?php
apcu_store('foobar', 2);
echo '$foobar = 2', PHP_EOL;
echo '$foobar == 1 ? 2 : 1 = ', (apcu_cas('foobar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;
echo '$foobar == 2 ? 1 : 2 = ', (apcu_cas('foobar', 2, 1) ? 'ok' : 'fail'), PHP_EOL;

echo '$foobar = ', apcu_fetch('foobar'), PHP_EOL;

echo '$f__bar == 1 ? 2 : 1 = ', (apcu_cas('f__bar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;

apcu_store('perfection', 'xyz');
echo '$perfection == 2 ? 1 : 2 = ', (apcu_cas('perfection', 2, 1) ? 'ok' : 'epic fail'), PHP_EOL;

echo '$foobar = ', apcu_fetch('foobar'), PHP_EOL;
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [apcu\_dec()](function.apcu-dec.md) \- Зменшити збережене число
-   [apcu\_store()](function.apcu-store.md) \- Кешує змінну
