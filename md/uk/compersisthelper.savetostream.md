---
navigation:
  - compersisthelper.savetofile.md: '« COMPersistHelper::SaveToFile'
  - class.com-exception.md: comexception »
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::SaveToStream'
---
# COMPersistHelper::SaveToStream

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::SaveToStream — Зберігає об'єкт у потоці

### Опис

```methodsynopsis
public COMPersistHelper::SaveToStream(resource $stream): bool
```

Зберігає об'єкт у заданому потоці.

### Список параметрів

`stream`

Потоковий ресурс.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [comexception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStream**або якщо виклик **IPersistStream::Save()** завершився помилкою.
