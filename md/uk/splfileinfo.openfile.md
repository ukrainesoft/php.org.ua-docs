---
navigation:
  - splfileinfo.iswritable.md: '« SplFileInfo::isWritable'
  - splfileinfo.setfileclass.md: 'SplFileInfo::setFileClass »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::openFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::openFile

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

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

Если установлено в\*\*`true`\*\*, имя файла также ищется в[include\_path](ini.core.md#ini.include-path)

`context`

Для описания`контекстів`обратитесь к следующему разделу руководства:[контекст](context.md)

### Значення, що повертаються

Відкритий файл як об'єкт (object) [SplFileObject](class.splfileobject.md)

### Помилки

Викидає [RuntimeException](class.runtimeexception.md), якщо файл не може бути відкритий (наприклад, недостатньо прав доступу).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `context` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**SplFileInfo::openFile()\*\*\*\*

```php
<?php
$fileinfo = new SplFileInfo('/tmp/foo.txt');

if ($fileinfo->isWritable()) {

    $fileobj = $fileinfo->openFile('a');

    $fileobj->fwrite("образец текста");
}
?>
```

### Дивіться також

-   [SplFileObject](class.splfileobject.md)
-   [stream\_context\_create()](function.stream-context-create.md) \- Створює контекст потоку
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
