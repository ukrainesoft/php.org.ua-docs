Приклади

-   [« Типи ресурсів](v8js.resources.html)
    
-   [V8Js »](class.v8js.html)
    
-   [PHP Manual](index.html)
    
-   [V8js](book.v8js.html)
    
-   Приклади
    

# Приклади

Основи використання

**Приклад #1 Запуск Javascript**

```php
<?php

$v8 = new V8Js();

/* basic.js */
$JS = <<< EOT
len = print('Hello' + ' ' + 'World!' + "\\n");
len;
EOT;

try {
  var_dump($v8->executeString($JS, 'basic.js'));
} catch (V8JsException $e) {
  var_dump($e);
}

?>
```

Результат виконання цього прикладу:

```
Hello World!
int(13)
```