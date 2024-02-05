---
navigation:
  - splfileobject.setmaxlinelen.md: '« SplFileObject::setMaxLineLen'
  - splfileobject.valid.md: 'SplFileObject::valid »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::\_\_function toString() { \[native code\] }

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::\_\_toString — Повертає поточний рядок у вигляді рядка

### Опис

```methodsynopsis
public SplFileObject::__toString(): string
```

Метод повертає поточний рядок у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний рядок у вигляді рядка.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.14, 8.2.1 | Змінено з псевдоніма [SplFileObject::fgets()](splfileobject.fgets.md) на реалізацію [SplFileObject::current()](splfileobject.current.md), яка повертає рядок CSV, коли встановлено прапор **`SplFileObject::READ_CSV`** |
| 7.2.19, 7.3.6 | Змінено псевдонім з [SplFileObject::current()](splfileobject.current.md)на[SplFileObject::fgets()](splfileobject.fgets.md) |
