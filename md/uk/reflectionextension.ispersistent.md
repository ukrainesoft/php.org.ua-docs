---
navigation:
  - reflectionextension.info.md: '« ReflectionExtension::info'
  - reflectionextension.istemporary.md: 'ReflectionExtension::isTemporary »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::isPersistent'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::isPersistent

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionExtension::isPersistent — Визначає, чи модуль постійний

### Опис

```methodsynopsis
public ReflectionExtension::isPersistent(): bool
```

Перевіряє, чи модуль постійний

Модуль є незмінним, якщо він завантажується за допомогою php.ini. Модуль є тимчасовим, а не постійним, якщо він завантажується за допомогою функції [dl()](function.dl.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** для модулів, що завантажуються через ini-налаштування [`extension`](ini.core.md#ini.extension) **`false`** в іншому випадку.

### Дивіться також

-   [ReflectionExtension::isTemporary()](reflectionextension.istemporary.md) \- Визначає, чи модуль тимчасовим
