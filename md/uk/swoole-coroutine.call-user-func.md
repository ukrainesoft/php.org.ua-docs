---
navigation:
  - swoole-coroutine.call-user-func-array.md: '« Swoole\\Coroutine::call\_user\_func\_array'
  - swoole-coroutine.cli-wait.md: 'Swoole\\Coroutine::cli\_wait »'
  - index.md: PHP Manual
  - class.swoole-coroutine.md: Swoole\\Coroutine
title: 'Swoole\\Coroutine::call\_user\_func'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Coroutine::call\_user\_func

(PECL swoole >= 2.0.0)

Swoole\\Coroutine::call\_user\_func — Викликає callback-функцію, задану першим параметром

### Опис

```methodsynopsis
public static Swoole\Coroutine::call_user_func(callable $callback, mixed ...$args): mixed
```

Викликає `callback`\-функцію, задану першим параметром і передає параметри, що залишилися, як аргументи.

### Список параметрів

`callback`

Функция[callable](language.types.callable.md) для дзвінка.

`args`

Нуль або більше параметрів для передачі в callback-функцію.

### Значення, що повертаються
