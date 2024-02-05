---
navigation:
  - reflectionextension.ispersistent.md: '« ReflectionExtension::isPersistent'
  - reflectionextension.tostring.md: 'ReflectionExtension::\_\_toString »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::isTemporary'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::isTemporary

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionExtension::isTemporary — Визначає, чи модуль є тимчасовим

### Опис

```methodsynopsis
public ReflectionExtension::isTemporary(): bool
```

Перевіряє, чи модуль тимчасовим.

Модуль є тимчасовим, коли він завантажується за допомогою функції [dl()](function.dl.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** для модулів, завантажених функцією [dl()](function.dl.md) **`false`** в іншому випадку.

### Дивіться також

-   [ReflectionExtension::isPersistent()](reflectionextension.ispersistent.md) \- Визначає, чи модуль є постійним
