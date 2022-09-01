---
navigation:
  - class.swoole-coroutine.html: « SwooleCoroutine
  - swoole-coroutine.call-user-func.html: 'SwooleCoroutine::calluserfunc »'
  - index.md: PHP Manual
  - class.swoole-coroutine.html: SwooleCoroutine
title: 'SwooleCoroutine::calluserfuncarray'
---
# SwooleCoroutine::calluserfuncarray

(PECL swoole >= 2.0.0)

SwooleCoroutine::calluserfuncarray - Викликає callback-функцію з масивом параметрів

### Опис

```methodsynopsis
public static Swoole\Coroutine::call_user_func_array(callable $callback, array $param_array): mixed
```

Викликає callback-функцію, задану першим параметром з параметрами paramarray.

### Список параметрів

`callback`

Функція [callable](language.types.callable.md) для дзвінка.

`param_array`

Нуль або більше параметрів для передачі в callback-функцію.

### Значення, що повертаються
