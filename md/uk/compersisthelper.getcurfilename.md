---
navigation:
  - compersisthelper.construct.md: '« COMPersistHelper::\_\_construct'
  - compersisthelper.getmaxstreamsize.md: 'COMPersistHelper::GetMaxStreamSize »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::GetCurFileName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# COMPersistHelper::GetCurFileName

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::GetCurFileName — Отримати ім'я файлу

### Опис

```methodsynopsis
public COMPersistHelper::GetCurFileName(): string|false
```

Повертає назву файлу, пов'язаного з об'єктом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, пов'язаного з об'єктом.

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistFile**або якщо виклик **IPersistFile::GetCurFile()** завершився помилкою.
