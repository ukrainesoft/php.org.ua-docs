---
navigation:
  - splfileinfo.construct.md: '« SplFileInfo::construct'
  - splfileinfo.getbasename.md: 'SplFileInfo::getBasename »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getATime'
---
# SplFileInfo::getATime

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getATime — Отримує час останнього доступу до файлу

### Опис

```methodsynopsis
public SplFileInfo::getATime(): int|false
```

Отримує час останнього доступу до файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останнього звернення до файлу у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає [RunTimeException](class.runtimeexception.md) у разі виникнення помилки.

### Дивіться також

-   [fileatime()](function.fileatime.md) - Повертає час останнього доступу до файлу
