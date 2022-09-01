---
navigation:
  - splfileinfo.iswritable.md: '« SplFileInfo::isWritable'
  - splfileinfo.setfileclass.md: 'SplFileInfo::setFileClass »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::openFile'
---
# SplFileInfo::openFile

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::openFile — Отримує об'єкт SplFileObject для файлу

### Опис

```methodsynopsis
public SplFileInfo::openFile(string $mode = "r", bool $useIncludePath = false, ?resource $context = null): SplFileObject
```

Створює об'єкт (object) [SplFileObject](class.splfileobject.md) файлу. Це корисно, тому що [SplFileObject](class.splfileobject.md) містить додаткові методи для роботи з файлом, у той час як [SplFileInfo](class.splfileinfo.md) корисний тільки для отримання інформації, наприклад, чи файл для запису.

### Список параметрів

`mode`

Режим відкриття файлу. Дивіться документацію з [fopen()](function.fopen.md) із описом можливих режимів. За промовчанням лише для читання.

`useIncludePath`

Якщо встановлено **`true`**, ім'я файлу також шукається в [includepath](ini.core.html#ini.include-path)

`context`

Для опису `контекстов` зверніться до наступного розділу посібника: [контекст](context.md)

### Значення, що повертаються

Відкритий файл як об'єкт (object) [SplFileObject](class.splfileobject.md)

### Помилки

Викидає [RuntimeException](class.runtimeexception.md), якщо файл не може бути відкритий (наприклад, недостатньо прав доступу).

### список змін

| Версия | Описание |
| --- | --- |
|  | `context` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::openFile()****

```php
<?php
$fileinfo = new SplFileInfo('/tmp/foo.txt');

if ($fileinfo->isWritable()) {

    $fileobj = $fileinfo->openFile('a');

    $fileobj->fwrite("образец текста");
}
?>
```

### Дивіться також

-   [SplFileObject](class.splfileobject.md)
-   [streamcontextcreate()](function.stream-context-create.html) - Створює контекст потоку
-   [fopen()](function.fopen.md) - Відкриває файл або URL
