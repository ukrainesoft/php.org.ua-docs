---
navigation:
  - v8js.executestring.md: '« V8Js::executeString'
  - v8js.getpendingexception.md: 'V8Js::getPendingException »'
  - index.md: PHP Manual
  - class.v8js.md: V8Js
title: 'V8Js::getExtensions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# V8Js::getExtensions

(PECL v8js >= 0.1.0)

V8Js::getExtensions — Повертає масив зареєстрованих модулів

### Опис

```methodsynopsis
public static V8Js::getExtensions(): array
```

Повертає масив зареєстрованих за допомогою [V8Js::registerExtension()](v8js.registerextension.md)модулей Javascript.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив зареєстрованих модулів чи порожній масив, якщо їх немає.
