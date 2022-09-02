---
navigation:
  - splfileobject.fpassthru.md: '« SplFileObject::fpassthru'
  - splfileobject.fread.md: 'SplFileObject::fread »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fputcsv'
---
# SplFileObject::fputcsv

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SplFileObject::fputcsv — Записати масив полів у вигляді рядка CSV

### Опис

```methodsynopsis
public SplFileObject::fputcsv(    array $fields,    string $separator = ",",    string $enclosure = "\"",    string $escape = "\\",    string $eol = "\n"): int|false
```

Записує масив `fields` у файл як рядок CSV.

### Список параметрів

`fields`

Масив значень

`separator`

Необов'язковий параметр `separator` встановлює роздільник полів (лише один однобайтовий символ).

`enclosure`

Необов'язковий параметр `enclosure` (лише один однобайтовий символ). Символ обгортання використовується для розміщення значень полів. Наприклад, рядок 'рядок' обгорнутий в одиночні лапки (').

`escape`

Необов'язковий параметр `escape` встановлює символ екранування (не більше одного однобайтового символу). Порожня стрічка (`""`) відключає пропрієтарний механізм екранування.

`eol`

Необов'язковий параметр `eol` задає послідовність кінця рядка, що настроюється.

> **Зауваження**
> 
> Якщо символ `enclosure` міститься в полі, він буде екранований шляхом його подвоєння, якщо йому не передує `escape`

### Значення, що повертаються

Повертає довжину записаного рядка або **`false`** у разі виникнення помилки.

Повертає **`false`** і не здійснює запис у файл, якщо параметри `separator` або `enclosure` містять більше одного символу.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо параметри `separator` або `enclosure` містять більше одного символу.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано необов'язковий параметр `eol` |
|  | Тепер параметр `escape` може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |

### Приклади

**Приклад #1 Приклад **SplFileObject::fputcsv()****

```php
<?php

$list = array (
    array('aaa', 'bbb', 'ccc', 'dddd'),
    array('123', '456', '789'),
    array('"aaa"', '"bbb"')
);

$file = new SplFileObject('file.csv', 'w');

foreach ($list as $fields) {
    $file->fputcsv($fields);
}

?>
```

Приклад вище записує наступні рядки в `file.csv`

```
aaa,bbb,ccc,dddd
123,456,789
"""aaa""","""bbb"""
```

### Дивіться також

-   [fputcsv()](function.fputcsv.md) - Форматує рядок у вигляді CSV і записує його у файловий покажчик
-   [SplFileObject::fgetcsv()](splfileobject.fgetcsv.md) - Отримати рядок із файлу та його розбір як поля CSV
