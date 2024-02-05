---
navigation:
  - compersisthelper.loadfromfile.md: '« COMPersistHelper::LoadFromFile'
  - compersisthelper.savetofile.md: 'COMPersistHelper::SaveToFile »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::LoadFromStream'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# COMPersistHelper::LoadFromStream

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::LoadFromStream — Завантажує об'єкт із потоку

### Опис

```methodsynopsis
public COMPersistHelper::LoadFromStream(resource $stream): bool
```

Завантажує об'єкт із потоку, де його спочатку було збережено.

### Список параметрів

`stream`

Потоковий ресурс для завантаження об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStream**або якщо виклик **IPersistStream::Load()** завершився помилкою.
