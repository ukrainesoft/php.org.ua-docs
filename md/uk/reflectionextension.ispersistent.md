---
navigation:
  - reflectionextension.info.md: '« ReflectionExtension::info'
  - reflectionextension.istemporary.md: 'ReflectionExtension::isTemporary »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::isPersistent'
---
# ReflectionExtension::isPersistent

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionExtension::isPersistent — Визначає, чи модуль постійний

### Опис

```methodsynopsis
public ReflectionExtension::isPersistent(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** для модулів, що завантажуються через ini-налаштування [`extension`](ini.core.md#ini.extension) **`false`** в іншому випадку.

### Дивіться також

-   [ReflectionExtension::isTemporary()](reflectionextension.istemporary.md) - Визначає, чи модуль тимчасовим
