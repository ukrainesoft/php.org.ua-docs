Сканує дані із вказаного файлу та витягує всі вкладені файли, кодовані в uuencode

-   [« mailparsestreamencode](function.mailparse-stream-encode.html)
    
-   [Математичні модулі »](refs.math.md)
    
-   [PHP Manual](index.md)
    
-   [Mailparse](ref.mailparse.md)
    
-   Сканує дані із вказаного файлу та витягує всі вкладені файли, кодовані в uuencode
    

# mailparseuudecodeall

(PECL mailparse >= 0.9.0)

mailparseuudecodeall — Сканує дані із вказаного файлу та витягує всі вкладені файли, кодовані в uuencode

### Опис

```methodsynopsis
mailparse_uudecode_all(resource $fp): array
```

Сканує дані із вказаного файлу та витягує всі вкладені файли, кодовані в uuencode, у тимчасові файли.

### Список параметрів

`fp`

Файловий дескриптор.

### Значення, що повертаються

Повертає асоціативний масив, що містить інформацію щодо вилучених файлів.

<table class="doctable informaltable"><tbody class="tbody"><tr><td><code class="literal">filename</code></td><td>Шлях до створеного тимчасового файлу</td></tr><tr><td><code class="literal">origfilename</code></td><td>Оригінальне ім'я файлу тільки для кодованих uuencode</td></tr></tbody></table>

Перший елемент міститиме тіло повідомлення. Усі наступні - інформацію щодо вилучених вкладень.

### Приклади

**Приклад #1 Приклад використання **mailparseuudecodeall()****

```php
<?php

$text = <<<EOD
To: fred@example.com

hello, this is some text hello.
blah blah blah.

begin 644 test.txt
/=&AI<R!I<R!A('1E<W0*
`
end

EOD;

$fp = tmpfile();
fwrite($fp, $text);

$data = mailparse_uudecode_all($fp);

echo "BODY\n";
readfile($data[0]["filename"]);
echo "UUE ({$data[1]['origfilename']})\n";
readfile($data[1]["filename"]);

// Очищаем
unlink($data[0]["filename"]);
unlink($data[1]["filename"]);

?>
```

Результат виконання цього прикладу:

```
BODY
To: fred@example.com

hello, this is some text hello.
blah blah blah.

UUE (test.txt)
this is a test
```