---
navigation:
  - v8js.getextensions.md: '« V8Js::getExtensions'
  - v8js.registerextension.md: 'V8Js::registerExtension »'
  - index.md: PHP Manual
  - class.v8js.md: V8Js
title: 'V8Js::getPendingException'
---
# V8Js::getPendingException

(PECL v8js >= 0.1.0)

V8Js::getPendingException — Повертає очікуваний непойманий виняток Javascript

### Опис

```methodsynopsis
public V8Js::getPendingException(): V8JsException
```

Повертає очікуваний непойманий виняток Javascript у вигляді [V8JsException](class.v8jsexception.md), що залишилося від попередніх запусків [V8Js::executeString()](v8js.executestring.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[V8JsException](class.v8jsexception.md) або **`null`**
