---
navigation:
  - function.apcu-fetch.md: « apcu\_fetch
  - function.apcu-key-info.md: apcu\_key\_info »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_inc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_inc

(PECL apcu >= 4.0.0)

apcu\_inc — Збільшити збережене число

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

Повертає поточне значення `key` у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки

### Приклади

**Приклад #1 Приклад використання** apcu\_inc()\*\*\*\*

```php
<?php
echo "Сделаем что-то без ошибки", PHP_EOL;

apcu_store('anumber', 42);

echo apcu_fetch('anumber'), PHP_EOL;

echo apcu_inc('anumber'), PHP_EOL;
echo apcu_inc('anumber', 10), PHP_EOL;
echo apcu_inc('anumber', 10, $success), PHP_EOL;

var_dump($success);

echo "А теперь с ошибкой", PHP_EOL, PHP_EOL;

apcu_store('astring', 'foo');

$ret = apcu_inc('astring', 1, $fail);

var_dump($ret);
var_dump($fail);
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [apcu\_dec()](function.apcu-dec.md) \- Зменшити збережене число
