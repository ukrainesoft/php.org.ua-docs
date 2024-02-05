---
navigation:
  - splfileinfo.getextension.md: '« SplFileInfo::getExtension'
  - splfileinfo.getfilename.md: 'SplFileInfo::getFilename »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getFileInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getFileInfo

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getFileInfo — Отримує об'єкт SplFileInfo для файлу

### Опис

```methodsynopsis
public SplFileInfo::getFileInfo(?string $class = null): SplFileInfo
```

Цей метод отримує об'єкт [SplFileInfo](class.splfileinfo.md)для указанного файла.

### Список параметрів

`class`

Ім'я похідного від [SplFileInfo](class.splfileinfo.md)класса для использования.

### Значення, що повертаються

Об'єкт [SplFileInfo](class.splfileinfo.md)створений для файлу.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `class` тепер допускає значення null. |

### Дивіться також

-   [SplFileInfo::setInfoClass()](splfileinfo.setinfoclass.md) \- Вказує ім'я класу, об'єкти якого будуть створюватися методами SplFileInfo::getFileInfo та SplFileInfo::getPathInfo
