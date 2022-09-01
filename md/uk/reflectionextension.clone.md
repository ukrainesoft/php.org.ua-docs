---
navigation:
  - class.reflectionextension.html: « ReflectionExtension
  - reflectionextension.construct.html: 'ReflectionExtension::construct »'
  - index.html: PHP Manual
  - class.reflectionextension.html: ReflectionExtension
title: 'ReflectionExtension::clone'
---
# ReflectionExtension::clone

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::clone — Клонує об'єкт

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

| Версия | Описание |
| --- | --- |
|  | Метод не є остаточним (final). |

### Дивіться також

-   [ReflectionExtension::construct()](reflectionextension.construct.md) - Створює об'єкт класу ReflectionExtension
-   [Клонування об'єктів](language.oop5.cloning.md)
