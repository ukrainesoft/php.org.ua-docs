---
navigation:
  - function.apcu-clear-cache.md: « apcu\_clear\_cache
  - function.apcu-delete.md: apcu\_delete »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_dec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_dec

(PECL apcu >= 4.0.0)

apcu\_dec — Зменшити збережене число

### Опис

```methodsynopsis
apcu_dec(    string $key,    int $step = 1,    bool &$success = ?,    int $ttl = 0): int|false
```

Зменшує збережене число.

### Список параметрів

`key`

Ключ значення, яке треба зменшити.

`step`

Величина, яку необхідно зменшити.

`success`

Необов'язковий параметр. Якщо заданий, то в нього буде записано логічне значення \*\*`true`**или**`false`\*\*в зависимости от успешности операции уменьшения.

`ttl`

TTL(час життя), що використовується, якщо операція вставляє нове значення (а не зменшує існуюче).

### Значення, що повертаються

Повертає поточне значення `key` у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки

### Приклади

**Пример #1 Пример использования**apcu\_dec()\*\*\*\*

```php
<?php
echo "Сделаем что-то без ошибки", PHP_EOL;

apcu_store('anumber', 42);

echo apcu_fetch('anumber'), PHP_EOL;

echo apcu_dec('anumber'), PHP_EOL;
echo apcu_dec('anumber', 10), PHP_EOL;
echo apcu_dec('anumber', 10, $success), PHP_EOL;

var_dump($success);

echo "А теперь с ошибкой", PHP_EOL, PHP_EOL;

apcu_store('astring', 'foo');

$ret = apcu_dec('astring', 1, $fail);

var_dump($ret);
var_dump($fail);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Сделаем что-то без ошибки
42
41
31
21
bool(true)
А теперь с ошибкой

bool(false)
bool(false)
```

### Дивіться також

-   [apcu\_inc()](function.apcu-inc.md) \- Збільшити збережене число
