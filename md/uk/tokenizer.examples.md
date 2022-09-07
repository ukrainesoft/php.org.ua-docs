---
navigation:
  - tokenizer.constants.md: « Обумовлені константи
  - class.phptoken.md: PhpToken »
  - index.md: PHP Manual
  - book.tokenizer.md: Лексер (Tokenizer)
title: Приклади
---
# Приклади

Простий приклад PHP-скрипту, який використовує tokenizer (лексер), який читає PHP-файл, видаляє всі коментарі з вихідного коду та виводить лише чистий код.

**Приклад #1 Видалення коментарів лексером**

```php
<?php
$source = file_get_contents('example.php');
$tokens = token_get_all($source);

foreach ($tokens as $token) {
   if (is_string($token)) {
       // простая однабуквенная лексема
       echo $token;
   } else {
       // Масив с лексемой
       list($id, $text) = $token;

       switch ($id) {
           case T_DOC_COMMENT:
               // нет действий для комментариев
               break;

           default:
               // все остальное -> выводим как есть
               echo $text;
               break;
       }
   }
}
?>
```
