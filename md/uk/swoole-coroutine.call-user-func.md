Викликає callback-функцію, задану першим параметром

-   [« SwooleCoroutine::calluserfuncarray](swoole-coroutine.call-user-func-array.html)
    
-   [SwooleCoroutine::cliwait »](swoole-coroutine.cli-wait.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleCoroutine](class.swoole-coroutine.html)
    
-   Викликає callback-функцію, задану першим параметром
    

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