---
navigation:
  - compersisthelper.getmaxstreamsize.md: '« COMPersistHelper::GetMaxStreamSize'
  - compersisthelper.loadfromfile.md: 'COMPersistHelper::LoadFromFile »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::InitNew'
---
# COMPersistHelper::InitNew

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::InitNew — Ініціалізує об'єкт у стан за замовчуванням

### Опис

```methodsynopsis
public COMPersistHelper::InitNew(): bool
```

Ініціалізує об'єкт у стан за замовчуванням.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [comexception](class.com-exception.html)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStreamInit**або якщо виклик **IPersistStreamInit::Init()** завершився помилкою.
