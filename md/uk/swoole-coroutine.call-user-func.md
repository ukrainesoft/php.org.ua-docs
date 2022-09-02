---
navigation:
  - swoole-coroutine.call-user-func-array.md: '« SwooleCoroutine::calluserfuncarray'
  - swoole-coroutine.cli-wait.md: 'SwooleCoroutine::cliwait »'
  - index.md: PHP Manual
  - class.swoole-coroutine.md: SwooleCoroutine
title: 'SwooleCoroutine::calluserfunc'
---
# SwooleCoroutine::calluserfunc

(PECL swoole >= 2.0.0)

SwooleCoroutine::calluserfunc — Викликає callback-функцію, задану першим параметром

### Опис

```methodsynopsis
public static Swoole\Coroutine::call_user_func(callable $callback, mixed ...$args): mixed
```

Викликає `callback`функцію, задану першим параметром і передає параметри, що залишилися, як аргументи.

### Список параметрів

`callback`

Функція [callable](language.types.callable.md) для дзвінка.

`args`

Нуль або більше параметрів для передачі в callback-функцію.

### Значення, що повертаються
