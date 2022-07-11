- [«Зумовлені константи](tokenizer.constants.md)
- [PhpToken »](class.phptoken.md)

- [PHP Manual](index.md)
- [Лексер (Tokenizer)](book.tokenizer.md)
- Приклади

# Приклади

Простий приклад PHP-скрипту, що використовує tokenizer (лексер), який
читає PHP-файл, видаляє всі коментарі з вихідного коду та виводить
лише чистий код.

**Приклад #1 Видалення коментарів лексером**

`<?php$source = file_get_contents('example.php');$tokens = token_get_all($source);foreach ($tokens as $token) {   if (is_string($token))              token; } else {        // масив з лексемою       list($id, $text) = $token; s                                   default:                // все остальное -> виводимо як є                 echo $text; break; }   }}?> `
