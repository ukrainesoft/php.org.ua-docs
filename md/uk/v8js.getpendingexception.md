Повертає очікуваний непойманий виняток Javascript

-   [« V8Js::getExtensions](v8js.getextensions.html)
    
-   [V8Js::registerExtension »](v8js.registerextension.html)
    
-   [PHP Manual](index.html)
    
-   [V8Js](class.v8js.html)
    
-   Повертає очікуваний непойманий виняток Javascript
    

# V8Js::getPendingException

(PECL v8js >= 0.1.0)

V8Js::getPendingException — Повертає очікуваний непойманий виняток Javascript

### Опис

```methodsynopsis
public V8Js::getPendingException(): V8JsException
```

Повертає очікуваний непойманий виняток Javascript у вигляді [V8JsException](class.v8jsexception.html), що залишилося від попередніх запусків [V8Js::executeString()](v8js.executestring.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[V8JsException](class.v8jsexception.html) або **`null`**