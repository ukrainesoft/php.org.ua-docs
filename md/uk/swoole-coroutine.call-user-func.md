---
navigation:
  - swoole-coroutine.call-user-func-array.html: '« SwooleCoroutine::calluserfuncarray'
  - swoole-coroutine.cli-wait.html: 'SwooleCoroutine::cliwait »'
  - index.html: PHP Manual
  - class.swoole-coroutine.html: SwooleCoroutine
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

Функція [callable](language.types.callable.html) для дзвінка.

`args`

Нуль або більше параметрів для передачі в callback-функцію.

### Значення, що повертаються
