---
navigation:
  - compersisthelper.construct.md: '« COMPersistHelper::construct'
  - compersisthelper.getmaxstreamsize.md: 'COMPersistHelper::GetMaxStreamSize »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::GetCurFileName'
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

Викидає виняток [comexception](class.com-exception.html)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistFile**або якщо виклик **IPersistFile::GetCurFile()** завершився помилкою.
