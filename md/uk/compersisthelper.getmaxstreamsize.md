---
navigation:
  - compersisthelper.getcurfilename.md: '« COMPersistHelper::GetCurFileName'
  - compersisthelper.initnew.md: 'COMPersistHelper::InitNew »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::GetMaxStreamSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# COMPersistHelper::GetMaxStreamSize

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::GetMaxStreamSize — Отримати максимальний розмір потоку

### Опис

```methodsynopsis
public COMPersistHelper::GetMaxStreamSize(): int
```

Повертає розмір потоку (в байтах), необхідний збереження об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає розмір потоку (в байтах), необхідний збереження об'єкта.

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStreamInit**або якщо виклик **IPersistStream::GetSizeMax()** завершився помилкою.
