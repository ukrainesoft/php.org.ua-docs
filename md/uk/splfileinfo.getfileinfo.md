Отримує об'єкт SplFileInfo для файлу

-   [« SplFileInfo::getExtension](splfileinfo.getextension.md)
    
-   [SplFileInfo::getFilename »](splfileinfo.getfilename.md)
    
-   [PHP Manual](index.md)
    
-   [SplFileInfo](class.splfileinfo.md)
    
-   Отримує об'єкт SplFileInfo для файлу
    

# SplFileInfo::getFileInfo

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getFileInfo — Отримує об'єкт SplFileInfo для файлу

### Опис

```methodsynopsis
public SplFileInfo::getFileInfo(?string $class = null): SplFileInfo
```

Цей метод отримує об'єкт [SplFileInfo](class.splfileinfo.md) для вказаного файлу.

### Список параметрів

`class`

Ім'я похідного від [SplFileInfo](class.splfileinfo.md) клас для використання.

### Значення, що повертаються

Об'єкт [SplFileInfo](class.splfileinfo.md)створений для файлу.

### список змін

| Версия | Описание                              |
|--------|---------------------------------------|
|        | `class` тепер допускає значення null. |

### Дивіться також

-   [SplFileInfo::setInfoClass()](splfileinfo.setinfoclass.md) - Вказує ім'я класу, об'єкти якого будуть створюватися методами SplFileInfo::getFileInfo та SplFileInfo::getPathInfo