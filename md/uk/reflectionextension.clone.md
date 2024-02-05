---
navigation:
  - class.reflectionextension.md: « ReflectionExtension
  - reflectionextension.construct.md: 'ReflectionExtension::\_\_construct »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::\_\_clone'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::\_\_clone

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::\_\_clone — Клонує об'єкт

### Опис

```methodsynopsis
private ReflectionExtension::__clone(): void
```

Метод clone запобігає клонуванню об'єкта. Об'єкти reflection не можуть бути клоновані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод нічого не повертає, у разі виклику виникає рокова помилка.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Метод не є остаточним (final). |

### Дивіться також

-   [ReflectionExtension::\_\_construct()](reflectionextension.construct.md) \- Створює об'єкт класу ReflectionExtension
-   [Клонування об'єктів](language.oop5.cloning.md)
