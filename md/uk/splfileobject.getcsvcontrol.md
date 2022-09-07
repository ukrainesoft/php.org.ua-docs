---
navigation:
  - splfileobject.getchildren.md: '« SplFileObject::getChildren'
  - splfileobject.getcurrentline.md: 'SplFileObject::getCurrentLine »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::getCsvControl'
---
# SplFileObject::getCsvControl

(PHP 5> = 5.2.0, PHP 7, PHP 8)

SplFileObject::getCsvControl — Отримує символи роздільника, обгортання та екранування для CSV

### Опис

```methodsynopsis
public SplFileObject::getCsvControl(): array
```

Отримує символи роздільника, обгортання та екранування для CSV. Символ обгортання використовується для розміщення значень полів. Наприклад, рядок 'рядок' обгорнутий в одиночні лапки (').

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексний масив, що містить символи роздільника та обмежувача.

### список змін

| Версия | Описание |
| --- | --- |
|  | Як символ екранування можна використовувати порожній рядок. |
|  | Доданий символ екранування до результуючого масиву. |

### Приклади

**Приклад #1 Приклад використання **SplFileObject::getCsvControl()****

```php
<?php
$file = new SplFileObject("data.txt");
print_r($file->getCsvControl());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => ,
    [1] => "
    [2] => \
)
```

### Дивіться також

-   [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.md) - Встановлює символи роздільника, обгортання та екранування для CSV
-   [SplFileObject::fgetcsv()](splfileobject.fgetcsv.md) - Отримати рядок із файлу та його розбір як поля CSV
