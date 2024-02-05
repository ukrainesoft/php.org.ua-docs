---
navigation:
  - compersisthelper.getmaxstreamsize.md: '« COMPersistHelper::GetMaxStreamSize'
  - compersisthelper.loadfromfile.md: 'COMPersistHelper::LoadFromFile »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::InitNew'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStreamInit**або якщо виклик **IPersistStreamInit::Init()** завершився помилкою.
