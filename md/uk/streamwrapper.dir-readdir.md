Читання запису з дескриптора директорії

-   [« streamWrapper::diropendir](streamwrapper.dir-opendir.html)
    
-   [streamWrapper::dirrewinddir »](streamwrapper.dir-rewinddir.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Читання запису з дескриптора директорії
    

# streamWrapper::dirreaddir

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::dirreaddir - Читання запису з дескриптора директорії

### Опис

```methodsynopsis
public streamWrapper::dir_readdir(): string
```

Цей метод викликається у процесі виконання [readdir()](function.readdir.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повинна повертати рядок (string), що представляє ім'я наступного файлу, або \*\*`false`\*\*якщо наступного файлу немає.

> **Зауваження**
> 
> Значення, що повертається, буде наведено до типу string.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Приклади

**Приклад #1 Отримання списку файлів із tar-архівів**

```php
<?php
class streamWrapper {
    protected $fp;

    public function dir_opendir($path, $options) {
        $url = parse_url($path);

        $path = $url["host"] . $url["path"];

        if (!is_readable($path)) {
            trigger_error("Не могу прочитать $path ", E_USER_NOTICE);
            return false;
        }
        if (!is_file($path)) {
            trigger_error("$path не является файлом", E_USER_NOTICE);
            return false;
        }

        $this->fp = fopen($path, "rb");
        return true;
    }

    public function dir_readdir() {
        // Извлечение заголовка
        $header      = fread($this->fp, 512);
        $data = unpack("a100filename/a8mode/a8uid/a8gid/a12size/a12mtime/a8checksum/a1filetype/a100link/a100linkedfile", $header);

        // Убираем лишние пробелы в имени файла и его размере
        $filename    = trim($data["filename"]);

        // Нет файла? Значит мы дошли до конца архива
        if (!$filename) {
            return false;
        }

        $octal_bytes = trim($data["size"]);
        // Размер файла определён в восьмеричной системе
        $bytes       = octdec($octal_bytes);

        // tar округляет размеры файлов, чтобы они были
        // кратными 512 байтам (с заполнением нулями)
        $rest        = $bytes % 512;
        if ($rest > 0) {
            $bytes      += 512 - $rest;
        }

        // Перемещаемся внутри файла
        fseek($this->fp, $bytes, SEEK_CUR);

        return $filename;
    }

    public function dir_closedir() {
        return fclose($this->fp);
    }

    public function dir_rewinddir() {
        return fseek($this->fp, 0, SEEK_SET);
    }
}

stream_wrapper_register("tar", "streamWrapper");
$handle = opendir("tar://example.tar");
while (false !== ($file = readdir($handle))) {
    var_dump($file);
}

echo "Перемотка в начало..\n";
rewind($handle);
var_dump(readdir($handle));

closedir($handle);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(13) "construct.xml"
string(16) "dir-closedir.xml"
string(15) "dir-opendir.xml"
string(15) "dir-readdir.xml"
string(17) "dir-rewinddir.xml"
string(9) "mkdir.xml"
string(10) "rename.xml"
string(9) "rmdir.xml"
string(15) "stream-cast.xml"
string(16) "stream-close.xml"
string(14) "stream-eof.xml"
string(16) "stream-flush.xml"
string(15) "stream-lock.xml"
string(15) "stream-open.xml"
string(15) "stream-read.xml"
string(15) "stream-seek.xml"
string(21) "stream-set-option.xml"
string(15) "stream-stat.xml"
string(15) "stream-tell.xml"
string(16) "stream-write.xml"
string(10) "unlink.xml"
string(12) "url-stat.xml"
Rewinding..
string(13) "construct.xml"
```

### Дивіться також

-   [readdir()](function.readdir.html) - Отримує елемент каталогу за його дескриптором