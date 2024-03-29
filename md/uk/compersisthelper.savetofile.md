---
navigation:
  - compersisthelper.loadfromstream.md: '« COMPersistHelper::LoadFromStream'
  - compersisthelper.savetostream.md: 'COMPersistHelper::SaveToStream »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::SaveToFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# COMPersistHelper::SaveToFile

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::SaveToFile — Зберегти об'єкт у файл

### Опис

```methodsynopsis
public COMPersistHelper::SaveToFile(?string $filename, bool $remember = true): bool
```

Зберігає копію об'єкта у вказаний файл.

### Список параметрів

`filename`

Ім'я файлу.

`remember`

Визначає, чи буде `filename` використовуватись для поточного робочого файлу. Якщо **`true`**, то`filename` стає поточним файлом, і об'єкт повинен очистити свій прапор dirty після збереження. Якщо **`false`**, то ця операція запису буде вважатися як "Save A Copy As...". У цьому випадку поточний файл залишиться без змін та об'єкт не зніматиме прапор dirty.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistFile**або якщо виклик **IPersistFile::Save()** завершився помилкою.

### Приклади

**Приклад #1 Использование**COMPersistHelper::saveToFile()\*\*\*\*

```php
<?php
$word = new COM('Word.Application');
$doc = $word->Documents->Add();
$ph = new COMPersistHelper($doc);
$ph->SaveToFile('C:\\Users\\cmb\\Documents\\my.docx');
$word->Quit();
?>
```
