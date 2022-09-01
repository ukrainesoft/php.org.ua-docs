---
navigation:
  - compersisthelper.loadfromstream.html: '« COMPersistHelper::LoadFromStream'
  - compersisthelper.savetostream.html: 'COMPersistHelper::SaveToStream »'
  - index.html: PHP Manual
  - class.compersisthelper.html: COMPersistHelper
title: 'COMPersistHelper::SaveToFile'
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

Визначає, чи буде `filename` використовуватись для поточного робочого файлу. Якщо **`true`**, то `filename` стає поточним файлом, і об'єкт повинен очистити свій прапор dirty після збереження. Якщо **`false`**, то ця операція запису буде вважатися як "Save A Copy As...". У цьому випадку поточний файл залишиться без змін та об'єкт не зніматиме прапор dirty.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [comexception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistFile**або якщо виклик **IPersistFile::Save()** завершився помилкою.

### Приклади

**Приклад #1 Використання **COMPersistHelper::saveToFile()****

```php
<?php
$word = new COM('Word.Application');
$doc = $word->Documents->Add();
$ph = new COMPersistHelper($doc);
$ph->SaveToFile('C:\\Users\\cmb\\Documents\\my.docx');
$word->Quit();
?>
```
