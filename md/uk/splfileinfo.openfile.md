Отримує об'єкт SplFileObject для файлу

-   [« SplFileInfo::isWritable](splfileinfo.iswritable.html)
    
-   [SplFileInfo::setFileClass »](splfileinfo.setfileclass.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує об'єкт SplFileObject для файлу
    

# SplFileInfo::openFile

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::openFile — Отримує об'єкт SplFileObject для файлу

### Опис

```methodsynopsis
public SplFileInfo::openFile(string $mode = "r", bool $useIncludePath = false, ?resource $context = null): SplFileObject
```

Створює об'єкт (object) [SplFileObject](class.splfileobject.html) файлу. Це корисно, тому що [SplFileObject](class.splfileobject.html) містить додаткові методи для роботи з файлом, у той час як [SplFileInfo](class.splfileinfo.html) корисний тільки для отримання інформації, наприклад, чи файл для запису.

### Список параметрів

`mode`

Режим відкриття файлу. Дивіться документацію з [fopen()](function.fopen.html) із описом можливих режимів. За промовчанням лише для читання.

`useIncludePath`

Якщо встановлено **`true`**, ім'я файлу також шукається в [include\_path](ini.core.html#ini.include-path)

`context`

Для опису `контекстов` зверніться до наступного розділу посібника: [контекст](context.html)

### Значення, що повертаються

Відкритий файл як об'єкт (object) [SplFileObject](class.splfileobject.html)

### Помилки

Викидає [RuntimeException](class.runtimeexception.html), якщо файл не може бути відкритий (наприклад, недостатньо прав доступу).

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

-   [SplFileObject](class.splfileobject.html)
-   [stream\_context\_create()](function.stream-context-create.html) - Створює контекст потоку
-   [fopen()](function.fopen.html) - Відкриває файл або URL