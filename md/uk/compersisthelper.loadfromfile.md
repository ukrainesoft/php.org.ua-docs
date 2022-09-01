---
navigation:
  - compersisthelper.initnew.md: '« COMPersistHelper::InitNew'
  - compersisthelper.loadfromstream.md: 'COMPersistHelper::LoadFromStream »'
  - index.md: PHP Manual
  - class.compersisthelper.md: COMPersistHelper
title: 'COMPersistHelper::LoadFromFile'
---
# COMPersistHelper::LoadFromFile

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::LoadFromFile — Завантажити об'єкт із файлу

### Опис

```methodsynopsis
public COMPersistHelper::LoadFromFile(string $filename, int $flags = 0): bool
```

Відкриває вказаний файл та ініціалізує об'єкт із його вмісту.

### Список параметрів

`filename`

Ім'я файлу.

`flags`

Режим доступу для доступу до файлу. Допустимі значення вказані в [» перерахуванні STGM](https://docs.microsoft.com/en-us/windows/win32/stg/stgm-constants). Цей режим вважається бажаним, але може бути, за потреби, змінений на суворіший Якщо параметр `flags` заданий як `0`, то файл буде відкритий з дозволами за замовчуванням, які б використовувалися, якби користувач відкривав цей файл.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [comexception](class.com-exception.md)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistFile**або якщо виклик **IPersistFile::Load()** завершився помилкою.
