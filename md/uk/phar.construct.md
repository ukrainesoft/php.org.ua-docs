Створює об'єкт Phar-архіву

-   [« Phar::compressFiles](phar.compressfiles.html)
    
-   [Phar::convertToData »](phar.converttodata.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Створює об'єкт Phar-архіву
    

# Phar::construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::construct — Створює об'єкт Phar-архіву

### Опис

public **Phar::construct**(string `$filename`, int `$flags` = FilesystemIterator::SKIPDOTS | FilesystemIterator::UNIXPATHS, ?string `$alias` **`null`**

### Список параметрів

`filename`

Шлях до вже існуючого Phar-архіву або до архіву, який має бути створений. Розширення імені файлу має містити .phar.

`flags`

Прапори, які мають бути передані до батьківського класу [RecursiveDirectoryIterator](class.recursivedirectoryiterator.html)

`alias`

Псевдонім, за допомогою якого повинні здійснюватися посилання на цей Phar-архів у викликах, пов'язаних із функціоналом потоків.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.html), якщо був викликаний двічі, та виняток [UnexpectedValueException](class.unexpectedvalueexception.html)якщо phar-архів не може бути відкритий.

### Приклади

**Приклад #1 Приклад використання **Phar::construct()****

```php
<?php
try {
    $p = new Phar('/путь/к/my.phar', FilesystemIterator::CURRENT_AS_FILEINFO | FilesystemIterator::KEY_AS_FILENAME,
                  'my.phar');
} catch (UnexpectedValueException $e) {
    die('Не удалось открыть my.phar');
} catch (BadMethodCallException $e) {
    echo 'Технически это не может произойти';
}
// это теперь работает
echo file_get_contents('phar://my.phar/example.txt');
// и работает так же, как если бы мы ввели
echo file_get_contents('phar:///путь/к/my.phar/example.txt');
?>
```