---
navigation:
  - phar.compressfiles.md: '« Phar::compressFiles'
  - phar.converttodata.md: 'Phar::convertToData »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::\_\_construct — Створює об'єкт Phar-архіву

### Опис

public **Phar::\_\_construct**(string`$filename`, int`$flags`\= FilesystemIterator::SKIP\_DOTS | FilesystemIterator::UNIX\_PATHS, ?string`$alias` **`null`**) .

### Список параметрів

`filename`

Шлях до вже існуючого Phar-архіву або до архіву, який має бути створений. Розширення імені файлу має містити .phar.

`flags`

Прапори, які мають бути передані до батьківського класу [RecursiveDirectoryIterator](class.recursivedirectoryiterator.md)

`alias`

Псевдонім, за допомогою якого повинні здійснюватися посилання на цей Phar-архів у викликах, пов'язаних із функціоналом потоків.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), якщо був викликаний двічі, та виняток [UnexpectedValueException](class.unexpectedvalueexception.md)якщо phar-архів не може бути відкритий.

### Приклади

**Приклад #1 Приклад використання** Phar::\_\_construct()\*\*\*\*

```php
<?php
try {
    $p = new Phar('/путь/к/my.phar', FilesystemIterator::CURRENT_AS_FILEINFO | FilesystemIterator::KEY_AS_FILENAME,
                  'my.phar');
} catch (UnexpectedValueException $e) {
    die('Не удалось открыть my.phar');
} catch (BadMethodCallException $e) {
    echo 'Технически это не может произойти';
}
// это теперь работает
echo file_get_contents('phar://my.phar/example.txt');
// и работает так же, как если бы мы ввели
echo file_get_contents('phar:///путь/к/my.phar/example.txt');
?>
```
