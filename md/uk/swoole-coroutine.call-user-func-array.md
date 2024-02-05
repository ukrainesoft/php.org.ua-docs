---
navigation:
  - class.swoole-coroutine.md: « Swoole\\Coroutine
  - swoole-coroutine.call-user-func.md: 'Swoole\\Coroutine::call\_user\_func »'
  - index.md: PHP Manual
  - class.swoole-coroutine.md: Swoole\\Coroutine
title: 'Swoole\\Coroutine::call\_user\_func\_array'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Coroutine::call\_user\_func\_array

(PECL swoole >= 2.0.0)

Swoole\\Coroutine::call\_user\_func\_array - Викликає callback-функцію з масивом параметрів

### Опис

```methodsynopsis
public static Swoole\Coroutine::call_user_func_array(callable $callback, array $param_array): mixed
```

Викликає callback-функцію, задану першим параметром з параметрами param\_array.

### Список параметрів

`callback`

Функция[callable](language.types.callable.md) для дзвінка.

`param_array`

Нуль або більше параметрів для передачі в callback-функцію.

### Значення, що повертаються
