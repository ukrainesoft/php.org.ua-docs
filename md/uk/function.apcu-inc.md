---
navigation:
  - function.apcu-fetch.md: « apcufetch
  - function.apcu-key-info.md: apcukeyinfo »
  - index.md: PHP Manual
  - ref.apcu.md: Функции APCu
title: apcuinc
---
# apcuinc

(PECL apcu >= 4.0.0)

apcuinc — Збільшити збережене число

### Опис

```methodsynopsis
apcu_inc(    string $key,    int $step = 1,    bool &$success = ?,    int $ttl = 0): int|false
```

Збільшує збережене число.

### Список параметрів

`key`

Ключ значення, яке треба збільшити.

`step`

Величина, яку необхідно збільшити.

`success`

Необов'язковий параметр. Якщо заданий, то в нього буде записано логічне значення **`true`** або **`false`** залежно від успішності операції збільшення.

`ttl`

TTL (час життя), що використовується, якщо операція вставляє нове значення (а не збільшує існуюче).

### Значення, що повертаються

Повертає поточне значення `key` у разі успішного виконання або **`false`** у разі виникнення помилки

### Приклади

**Приклад #1 Приклад використання **apcuinc()****

```php
<?php
echo "Сделаем что-то без ошибки", PHP_EOL;

apcu_store('anumber', 42);

echo apcu_fetch('anumber'), PHP_EOL;

echo apcu_inc('anumber'), PHP_EOL;
echo apcu_inc('anumber', 10), PHP_EOL;
echo apcu_inc('anumber', 10, $success), PHP_EOL;

var_dump($success);

echo "А теперь с ошибкой", PHP_EOL, PHP_EOL;

apcu_store('astring', 'foo');

$ret = apcu_inc('astring', 1, $fail);

var_dump($ret);
var_dump($fail);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Сделаем что-то без ошибки
42
43
53
63
bool(true)
А теперь с ошибкой

bool(false)
bool(false)
```

### Дивіться також

-   [apcudec()](function.apcu-dec.md) - Зменшити збережене число
