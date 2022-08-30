Викликає callback-функцію з масивом параметрів

-   [« SwooleCoroutine](class.swoole-coroutine.html)
    
-   [SwooleCoroutine::calluserfunc »](swoole-coroutine.call-user-func.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleCoroutine](class.swoole-coroutine.html)
    
-   Викликає callback-функцію з масивом параметрів
    

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

Функція [callable](language.types.callable.html) для дзвінка.

`param_array`

Нуль або більше параметрів для передачі в callback-функцію.

### Значення, що повертаються