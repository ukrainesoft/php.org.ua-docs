Приклад класу, зареєстрованого як обгортка потоку

-   [« Примеры](stream.examples.html)
    
-   [php\_user\_filter »](class.php-user-filter.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](stream.examples.html)
    
-   Приклад класу, зареєстрованого як обгортка потоку
    

## Приклад класу, зареєстрованого як обгортка потоку

Приклад нижче реалізує обробник протоколу var://, який дозволяє читати/писати в іменовану глобальну змінну, використовуючи стандартні потокові функції, що працюють із файловою системою, такі як [fread()](function.fread.html). Протокол var:// при передачі URL "var://foo" читатиме/писати з/в $GLOBALS"foo"

**Приклад #1 Потік для читання/запису глобальних змінних**

```php
<?php

class VariableStream {
    var $position;
    var $varname;

    function stream_open($path, $mode, $options, &$opened_path)
    {
        $url = parse_url($path);
        $this->varname = $url["host"];
        $this->position = 0;

        return true;
    }

    function stream_read($count)
    {
        $ret = substr($GLOBALS[$this->varname], $this->position, $count);
        $this->position += strlen($ret);
        return $ret;
    }

    function stream_write($data)
    {
        $left = substr($GLOBALS[$this->varname], 0, $this->position);
        $right = substr($GLOBALS[$this->varname], $this->position + strlen($data));
        $GLOBALS[$this->varname] = $left . $data . $right;
        $this->position += strlen($data);
        return strlen($data);
    }

    function stream_tell()
    {
        return $this->position;
    }

    function stream_eof()
    {
        return $this->position >= strlen($GLOBALS[$this->varname]);
    }

    function stream_seek($offset, $whence)
    {
        switch ($whence) {
            case SEEK_SET:
                if ($offset < strlen($GLOBALS[$this->varname]) && $offset >= 0) {
                     $this->position = $offset;
                     return true;
                } else {
                     return false;
                }
                break;

            case SEEK_CUR:
                if ($offset >= 0) {
                     $this->position += $offset;
                     return true;
                } else {
                     return false;
                }
                break;

            case SEEK_END:
                if (strlen($GLOBALS[$this->varname]) + $offset >= 0) {
                     $this->position = strlen($GLOBALS[$this->varname]) + $offset;
                     return true;
                } else {
                     return false;
                }
                break;

            default:
                return false;
        }
    }

    function stream_metadata($path, $option, $var)
    {
        if($option == STREAM_META_TOUCH) {
            $url = parse_url($path);
            $varname = $url["host"];
            if(!isset($GLOBALS[$varname])) {
                $GLOBALS[$varname] = '';
            }
            return true;
        }
        return false;
    }
}

stream_wrapper_register("var", "VariableStream")
    or die("Не удалось зарегистрировать обёртку");

$myvar = "";

$fp = fopen("var://myvar", "r+");

fwrite($fp, "line1\n");
fwrite($fp, "line2\n");
fwrite($fp, "line3\n");

rewind($fp);
while (!feof($fp)) {
    echo fgets($fp);
}
fclose($fp);
var_dump($myvar);

?>
```

Результат виконання цього прикладу:

```
line1
line2
line3
string(18) "line1
line2
line3
"
```