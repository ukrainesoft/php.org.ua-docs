---
navigation:
  - compersisthelper.savetofile.md: '« COMPersistHelper::SaveToFile'
  - class.com-exception.md: com\_exception »
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::SaveToStream'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStream**або якщо виклик **IPersistStream::Save()** завершився помилкою.
