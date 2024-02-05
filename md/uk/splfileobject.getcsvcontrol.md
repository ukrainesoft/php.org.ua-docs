---
navigation:
  - splfileobject.getchildren.md: '« SplFileObject::getChildren'
  - splfileobject.getcurrentline.md: 'SplFileObject::getCurrentLine »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::getCsvControl'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::getCsvControl

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

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

| Версия | Опис |
| --- | --- |
| 7.4.0 | Як символ екранування можна використовувати порожній рядок. |
| 7.0.10 | Доданий символ екранування до результуючого масиву. |

### Приклади

**Пример #1 Пример использования**SplFileObject::getCsvControl()\*\*\*\*

```php
<?php
$file = new SplFileObject("data.txt");
print_r($file->getCsvControl());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => ,
    [1] => "
    [2] => \
)
```

### Дивіться також

-   [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.md) \- Встановлює символи роздільника, обгортання та екранування для CSV
-   [SplFileObject::fgetcsv()](splfileobject.fgetcsv.md) \- Отримати рядок із файлу та його розбір як поля CSV
